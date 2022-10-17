# chainlink-docker-compose
Simple docker-compose-based project to get quickly up and running a Chainlink node. This is intended mainly for development use, or at least should be enough to get you started with a working-as-is repository. However, it assumes basic Docker skills.

# How to use

1. Clone repository

1. Review `chainlink-goerli.env` and adapt accordingly. The committed environment file uses Goerli testnet. Also, the example uses a chainstack public Ethereum service node.

2. Build and run with docker-compose

* Build with default values, which you can adapt if needed inside the `Dockerfile`
```
docker-compose up --build
```

* First build with your own build args and then run:

```
$ docker-compose build --build-arg API_USER_EMAIL=my@test.com API_USER_PASSWORD=mypassword

$ docker-compose up
```

4. Browse to `localhost:6688` and log in with your credentials.

Default credentials:
- username: `user@example.com`
- password: `PA@SSword1234!567`
- wallet password: `PA@SSword1234!567`