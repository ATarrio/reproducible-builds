# powpeg-node VETIVER-9.0.2.0

* Source: https://github.com/rsksmart/powpeg-node
* Branch: `VETIVER-9.0.2.0`

## Build

```
$ docker build -t powpeg-node/vetiver-9.0.2.0 .
```

## Verify

The last step of the build prints the sha256sum of the files, if, for any reason there's a need to recheck the hash the following commands can be used to generate them.

```
$ docker run --rm powpeg-node/vetiver-9.0.2.0 bash -c 'sha256sum * | grep -v javadoc.jar'
2db20e5b937ef5abe61bce901ba0a667dff9e0041464712d56f49d508a65a5ed  federate-node-VETIVER-9.0.2.0-all.jar
0342782596efc0a9817aba5e2182c494357dcbd073b6b68e47886d4f652c9745  federate-node-VETIVER-9.0.2.0.jar
37cf0ea8c5ea9d8f745af1a36c545f81a61df5d28f6c1ad0a99e1c36a69ac9e8  federate-node-VETIVER-9.0.2.0-sources.jar
```

## (Optional) Extract JAR from image

```
$ cid=$(docker run -d powpeg-node/vetiver-9.0.2.0 /bin/true)
$ docker cp "$cid":/home/rsk/ ./libs/
$ docker rm "$cid"
```
