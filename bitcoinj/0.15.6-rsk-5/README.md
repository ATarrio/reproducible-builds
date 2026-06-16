# BitcoinJ 0.15.6-rsk-5

* Source: https://github.com/rsksmart/bitcoinj
* Tag: `v0.15.6-rsk-5`

## Build

```
$ docker build -t bitcoinj/0.15.6-rsk-5 .
```

## Verify

```
$ docker run --rm bitcoinj/0.15.6-rsk-5 sh -c 'sha256sum * | grep -v javadoc.jar'
811eb7435503d79b53ccede923504ddf0cdc2b179b653ccbadcb0812808a2c5e  bitcoinj-core-0.15.6-rsk-5-sources.jar
7ea86959f736cf6ad452d563e3c4e90a6b1deae74ff16c42cdfd98efaf7e6794  bitcoinj-core-0.15.6-rsk-5.jar
9840816c7f4be0e2f177994de43a5d4cee4e981a2d76f0533fb70830c2f381a7  bitcoinj-core-0.15.6-rsk-5.pom
```

## (Optional) Extract JAR from image

```
$ docker run --name temp-container bitcoinj/0.15.6-rsk-5 /bin/true
$ docker cp temp-container:/home/bitcoinj/ ./libs
$ docker rm temp-container
```
