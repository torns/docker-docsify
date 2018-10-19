# docker-docsify

[Docsify](https://docsify.js.org/#/) server in a Docker container.

## Usage

To run locally:

```
$ docker build . -t quintondar/docsify
$ docker run -it -v $PWD:/docs:ro -p 3000:3000 docsify
```

To build your custom image:

```
FROM quintoandar/docsify
ADD . .
```

This image uses [tini](https://github.com/krallin/tini) to handle the docsify proccess, since tests showed that docsify alone would not timely respond to SIGTERM/SIGINT.
