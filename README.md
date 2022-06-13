# Auth JWT Devise

## System
1. Linux Ubuntu 20.04

## Installation

1. Clone repo to local

```
git clone https://github.com/aniket-k-kaushik/auth-jwt-devise.git
```

2. Install [rvm](https://rvm.io/) and
   [nvm](https://github.com/nvm-sh/nvm#installing-and-updating)

3. Install ruby 2.5.1

```
rvm install 2.5.1
```

4. Install Node 16.4.2

```
nvm install 16.4.2
```

5. Install Postgres

```
sudo apt install postgresql-12 libpq-dev
```

6. Create Username and password to access postgreSQL

```
sudo -u postgres createuser aniket -s   // In place of aniket you can give your name
```
```
sudo -u postgres psql
```
To set password for the new user we just created
```
postgres=# \password aniket   // aniket is the username 
```
Then Enter possword and re-enter it to confirm it.

7. Go to authentication-and-authorization/ds-assignment-backend

```
cd authentication-and-authorization/ds-assignment-backend
```

8. Install gem

```
bundle install
```

9. Install node packages

```
yarn install
```

10. Setup ENV's

Open .env

11. Update `DATABASE_URL` in `.env` as per local `psql` creds. For example, if
    the user is `aniket` and password is `aniket`, change the variable as
    `DATABASE_URL="postgres://aniket:aniket@localhost/ds-assignment-backend?encoding=utf8&pool=5&timeout=5000"`

12. Run `rake db:create` to create the database
```
rake db:create
```
14. Run `rake db:migrate` for migrations
```
rake db:migrate
```
16. Run `rake db:seed` for populating the database with initial data
```
rake db:seed
```

15. Run `rails s` to run rails server
```
rails s
```

16. Navigate to [http://127.0.0.1:3000/](http://127.0.0.1:3000/)
