# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

default: &default
  adapter: postgresql
  encoding: unicode
  host: db
  username: postgres
  password: changeme
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
development:
  <<: *default
  database: myapp_development
test:
  <<: *default
  database: myapp_test
production:
  <<: *default
  database: myapp_production

