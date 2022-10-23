# SolidityATL Chainlink Node
Docker-compose-based project to get quickly up and running a Chainlink node. 

We currently have a node running on Goerli:

- Oracle contract address: `0xAB770e728e4FDCF9CAE68B0BDC5548704156584c`
- Node address: `0x87ef7dAbf50Ce0d4033733ad1534d099187De99B`
- Node admin view: `http://147.182.216.198:6688/`

- There is a sample job on the deployed node that can be triggered:
  - JobId: `3da67337-f8b7-437d-acd9-ca91fd928aec`
  - Sample job contract address: `0xcC1c770cF3a9C315b3AC8F24f7aA65dE5ab2a722`
# How to run locally

1. Clone repository

1. Review `chainlink-goerli.env` and adapt accordingly. The committed environment file uses Goerli testnet. You will need to provide your own `ETH_URL`, some popular providers are chainstack and infra

2. Build and run with docker-compose

* Build with default values, which you can adapt if needed inside the `Dockerfile`
```
docker-compose up --build -d
```

* If you wan a custom username/password and then run:

```
$ docker-compose build --build-arg API_USER_EMAIL=my@test.com API_USER_PASSWORD=mypassword

$ docker-compose up
```

4. Browse to `localhost:6688` and log in with your credentials.

Default credentials:
- username: `user@example.com`
- password: `PA@SSword1234!567`
- wallet password: `PA@SSword1234!567`