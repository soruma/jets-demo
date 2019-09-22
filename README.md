# Jets Project

This README would normally document whatever steps are necessary to get the application up and running.

Things you might want to cover:

* Dependencies
* Configuration
* Database setup
* How to run the test suite
* Deployment instructions

```bash
mysql -h <endpoint> -P <db port> -u <db user> -p <database name>
```

## AWS deploy(development mode)

IAM setting

https://rubyonjets.com/docs/extras/minimal-deploy-iam/

Edit .env.development.remote 

```env
DATABASE_URL=mysql2://<db user>:<password>@<endpoint><database name>?pool=5
```

```bash
JETS_ENV=development JETS_ENV_REMOTE=1 jets db:create db:migrate 
JETS_ENV=development jets deploy
```
