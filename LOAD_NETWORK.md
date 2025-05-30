## 0. Set Planetscale and irys_pk

```yml
      PS_HOST: "your.planetscale.host"
      PS_USERNAME: "your_planetscale_username"
      PS_PASSWORD: "your_planetscale_password"
      irys_pk: "some_private_key_here"
```

build wvm-lighthouse locally (temprorary solution)

```sh
docker build --network=host . -t wvm-lighthouse:local --build-arg FEATURES=wvm
```

## 1. Run

```sh
kurtosis run --enclave wvmlocaldevnet $PATH_TO_THE_PACKAGE --args-file network_params.yaml
```

## 2. Stop

```sh
kurtosis enclave stop wvmlocaldevnet
```

## 3. Clean

```sh
kurtosis enclave rm wvmlocaldevnet
```


## 4. Logs

Example of logs reading

```sh
kurtosis service logs wvmlocaldevnet el-1-reth-lighthouse
```