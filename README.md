# docker-docsify

```
$ docker build . -t docsify
$ docker run -it -v $PWD:/docs:ro -p 3000:3000 docsify
```

This image uses [tini](https://github.com/krallin/tini) to handle the docsify proccess, since tests showed that docsify alone would not timely respond to SIGTERM/SIGINT.
