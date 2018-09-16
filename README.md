ORBIS

  ### Simple, powerful online communities.

</div>



## What is ORBIS?

### Vision

It is difficult to grow, manage and measure the impact of online communities. Community owners need modern, chat-based communities but are running into scaling issues when their community grows beyond a few hundred members. It becomes hard to keep track of who's who, know what conversations are happening, and ensure that the community is staying healthy and productive.

ORBIS aims to be the best platform to build any kind of community online by combining the best of web 2.0 forums and real-time chat apps. With best-in-class moderation tooling, a single platform for all your communities, threaded conversations by default, community health monitoring (and much more to come), we think that we will be able to help more people start and grow the best online communities.



### Status



<div align="center">
  <img height="50px" src="public/img/cluster-1.svg" />
</div>


#### Getting the secrets

While the app will run without any secrets set up, you won't be able to sign in locally. To get that set up, copy the provided example secrets file to the real location:

```
cp now-secrets.example.json now-secrets.json
```

> Note: If you're an employee at Spectrum we've got a more complete list of secrets that also lets you upload images etc. in 1Password, search for "now-secrets.json" to find it.

Now you're ready to run the app locally and sign into your local instance!

### Running the app locally

#### Background services

Whenever you want to run Spectrum locally you have to have RethinkDB and Redis running in the background. First start rethinkdb like we did to migrate the database:

```sh
rethinkdb
```

Then (without closing the rethinkdb tab!) open another tab and start Redis:

```sh
redis-server
```

#### Start the servers

Depending on what you're trying to work on you'll need to start different servers. Generally, all servers run in development mode by doing `yarn run dev:<workername>`, e.g. `yarn run dev:hermes` to start the email worker.

No matter what you're trying to do though, you'll want to have the API running, so start that in a background tab:

```
yarn run dev:api
```

#### Develop the web UI

To develop the frontend and web UI run

```
yarn run dev:web
```

#### Develop the mobile apps

To start the mobile apps run:

```
yarn run dev:mobile
```

And then open either the iOS simulator or the Android simulator with

```sh
yarn run open:ios
# or
yarn run open:android
```


> Note: If something didn't work or you ran into troubles please submit PRs to improve this doc and keep it up to date!

<br />
<div align="center">
  <img height="200px" src="public/img/connect.svg" />
</div>

## License

BSD 3-Clause, see the [LICENSE](./LICENSE) file.

