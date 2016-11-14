This slide deck is based on the fantastic [reveal.js framework](https://github.com/hakimel/reveal.js).

## Quickstart

```
git clone https://github.com/brainstorm/slides-tmpl
npm install
npm start
```

## Generate PDF

The builtin reveal.js PDF converter does not work properly, therefore I would suggest using [decktape](https://github.com/astefanutti/decktape):

```
$ docker run --rm --net=host -v `pwd`:/slides astefanutti/decktape http://<ABOVE_NODEJS_INSTANCE_IP>:8000 slides.pdf
```

## Video of the talk

[![example youtube talk](http://img.youtube.com/vi/<YOUTUBE_HASH>/0.jpg)](http://www.youtube.com/watch?v=<YOUTUBE_HASH>)
