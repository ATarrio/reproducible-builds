# rskj VETIVER-9.0.3

* Source: https://github.com/rsksmart/rskj
* Tag: `VETIVER-9.0.3`

## Build

```
$ docker build -t rskj/9.0.3-vetiver .
```

## Verify

Run the following command to verify the sha256sum of the built artifacts matches the expected values:

```
$ docker run --rm rskj/9.0.3-vetiver sh -c 'sha256sum * | grep -v javadoc.jar'
b15fbccb9b1aa2cec082f6f68beeed23cbbcfcf1caf5d0099e4ad146e72b2135  rskj-core-9.0.3-VETIVER-all.jar
d5d23756aae842a10b7e237cca3ad7900bfdaf71c469f24b5772742a96d584d5  rskj-core-9.0.3-VETIVER-sources.jar
ad5c791752f328a3c6d272e924d67ba78939269e0e68b56f9987997fe8c80fb9  rskj-core-9.0.3-VETIVER.jar
576c3964105a1e2e542596e6ddd8c66c06adca81420866cd89f9a455a074c5ac  rskj-core-9.0.3-VETIVER.module
e71d4eed536cfeed21451086139d9c61cacd5de3ce61b3da7a13c94b5670f75f  rskj-core-9.0.3-VETIVER.pom
```

## (Optional) Run RSK Node
```
$ docker run -d rskj/9.0.3-vetiver
```

## (Optional) Extract JAR from image

```
$ cid=$(docker run -d rskj/9.0.3-vetiver /bin/true)
$ docker cp "$cid":/home/rsk/ ./libs/
$ docker rm "$cid"
```
