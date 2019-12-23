# Dayeon Luandry

## Spec
```
ruby: reference by .ruby-version
mysql: 5.7
```

## Get Start
**install ruby**
```ruby
brew update && brew install rbenv ruby-build

# add path to .zshrc
export PATH="$HOME/.rbenv/bin:$PATH"
eval "$(rbenv init - zsh)"
source ~/.zshrc
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