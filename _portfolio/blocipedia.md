---
layout: post
title: Blocipedia
thumbnail-path: "img/blocipedia.png"
short-description: A production quality wiki publishing site with premium features.
---

{:.center}
![]({{ site.baseurl }}/img/blocipedia.png)
A production quality Wiki Publishing site with Premium Features  

{:.center}
* [See code on Github](https://github.com/mikeMedis/blocipedia){:target="_blank"}

## Explanation

Blocipedia is a Rails app that allows Standard(free) or Premium(Paid) users to create and publish wikis for everyone to see . As a Premium user, you are able to create private wikis and add collaborators to your wikis for others to contribute them.

## Problem

Blocipedia allows Premium users to create private wikis and collaborators. Colloborators could be Standard or Premium users. Some issues that arose when implementing this feature were:

1. "How can a Standard User see Private wikis when added as a collaborator and only when they are collaborators to said wiki?"<br>
2. "How Can a Premium user search for users to add to wikis as collaborator?"<br>
3. "How can I charge a monthly fee for Premium user?"

## Solution

I was able to implement collaborators through using Has Many Through (HMT) model relationship.

``` ruby
class User < ActiveRecord::Base
  has_many :collaborators
  has_many :wikis, through: :collaborators
end
```

``` ruby
class Wiki < ActiveRecord::Base
  belongs_to :user
  has_many :collaborators
end
```

``` ruby
class Collaborator < ActiveRecord::Base
  belongs_to :user
  belongs_to :wiki
end
```

This allowed me to properly add users as collaborators to specific wikis. But now how would a Premium user be able to search and add another user as a collaborator?
For that I used a Form Option Helper ```collection_select``` to search through users and add them as a collaborator.

``` ruby
<div class="form-group">
  <%= f.label :Add_Collabs %>
  <%= f.collection_select :user_id, @users, :id, :username %>
  <%= f.submit "Save", class: 'btn btn-default' %>
</div>
```

Stripe Gem was used to implement the monthly fee for Premium users. When a user is initially charged as a Premium user, their User role is updated from Standard to Premium  in the Stripe Controller :

``` ruby
current_user.role = 'premium'
current_user.stripe_id = customer.id
current_user.save
```

Which then grants them permission to create private wikis and collaborator.

{:.center}
![]({{ site.baseurl }}/img/userprofileblocipedia.png)

## Results

Premium user is able to search through current users and chose them as collaborators to wikis with ease.
User is able to create private wikis after upgrading to Premium

## Conclusion

The Blocipedia project allowed me to learn about many new Gems like Stripe for charging users and Devise to authenticate and create user sessions.
