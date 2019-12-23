# Dayeon Luandry

## Spec
```
ruby: reference by .ruby-version
mysql: 5.7
```

## Get Start
**ruby installation**
```ruby
brew update && brew install rbenv ruby-build

# add path to .zshrc
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init - zsh)"
source ~/.zshrc
```
**mysql installation**
```
brew install mysql@5.7
```

**show database erd**
```ruby
bundle exec erd
open doc/erd.png
```

**start project**
```ruby
cd dayeon-luandry

rbenv install $(cat .ruby-version)
bundle install --path=vendor/bundle
bundle exec rake db:create:migrate:seed
bundle exec rspec
```

**start service**
```ruby
bundle exec rails s # start from port 3000
```