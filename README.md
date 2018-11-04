### Hobo
---
https://github.com/Hobo

http://cookbook.hobocentral.net/tutorials/agility

```
sudo apt-get update
sudo apt-get install -y ruby1.9.3 rubygems nodejs libsqlite3-dev git
export GEM_HOME=$HOME/.gem
echo "export GEM_HOME=$HOME/.gem" >> .bashrc
PATH="$HOME/.gem/bin:$PATH"
echo 'PATH="$HOME/.gem/bin:$PATH"' >> .bashrc

gem install hobo
echo $HOBODEV
unset HOBODEV
hobo new thingybob --setup

cd thingbob
hobo g resource thing name:string body:text
hobo g migration
rails s
curl http://localhost:3000

```

```ruby
def create_permitted?
  acting_user.administrator?
end

def create_permitted?
  acting_user.signed_up?
end

Story.find(:first).status.class

has_many :contributor_memberships, :class_name => "ProjectMembership", :scope => :contributor
has_many :contributors, :through => :contributor_memberships, :source => :user

def accepts_changes_from?(user)
  user.administrator? || user == owner || user.in?(contributors)
end


```

```
<section param="content-body">

<show-page>
  <content_body:>Hello!</content-body:>
</show-page>

```
