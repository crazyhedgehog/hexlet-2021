# Telegram Bot 

A simple telegram bot that allows to study endlish words.  

## Description

Bot has the following functionality:
- A user can start/stop the studying process. 

## Getting Started

### Gems
```
gem 'activerecord'
gem 'dotenv'     # for using env. variables
gem 'multi_json'
gem 'nanoc', '~> 4.12'
gem 'pry', '~> 0.14.1'
gem 'puma'
gem 'rake', '~> 13.0.3'
gem 'robocop'
gem 'rspec'      # for running tests
gem 'sinatra'
gem 'sinatra-activerecord', '~> 2.0'
gem 'singleton'
gem 'sqlite3'    # db for testing
gem 'telegram-bot-ruby'
gem 'whenever', require: false
```
### Before executing
```
Run tunels using ngrok tool for server emulating:
1. ./ngrok authtoken {ngrok_token}
   ./ngrok http {port}
Send post request to telegram API that allows to redirect
2. curl --location --request POST 'https://api.telegram.org/bot{token}/setWebhook' --header 'Content-Type: application/json' --data-raw '{"url": {url}}'
```

### Executing program

* Run ``` bundle install ```
* Run ``` bundle exec rake db:seed ```
* Run ``` bundle exec rake db:migrate ```
* Run ``` bundle exec rake db:seed ```
* Run ``` rackup -p {port} ```

### Task for cron
* Start ``` whenever --update-crontab --set environment='development' ```
* Stop ``` whenever --clear-crontab ```