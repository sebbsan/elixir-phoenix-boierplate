# Discuss

## Pre-Requisites

The App is configured to run with Postges. Configure your local Postgres connection through amending the following parts the file `config/dev.exs`:

```
config :discuss, Discuss.Repo,
  adapter: Ecto.Adapters.Postgres,
  username: "<your postgres user name>",
  password: "<your postres password>",
  database: "<your postgres db>",
  hostname: "localhost",
  pool_size: 10
```

The App is currently using Github OAuth to log in. You have to register the application in Github and add the key / secret with in the file `config/dev.secret.exs` like so:

```
use Mix.Config

config :ueberauth, Ueberauth.Strategy.Github.OAuth,
  client_id: "<your github client id>",
  client_secret: "<your github client secret>"

```


To start your Phoenix app:

  * Install dependencies with `mix deps.get`
  * Create and migrate your database with `mix ecto.create && mix ecto.migrate`
  * Install Node.js dependencies with `npm install`
  * Start Phoenix endpoint with `mix phoenix.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](http://www.phoenixframework.org/docs/deployment).

## Learn more

  * Official website: http://www.phoenixframework.org/
  * Guides: http://phoenixframework.org/docs/overview
  * Docs: https://hexdocs.pm/phoenix
  * Mailing list: http://groups.google.com/group/phoenix-talk
  * Source: https://github.com/phoenixframework/phoenix
