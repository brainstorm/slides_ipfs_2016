This slide deck is based on the fantastic [reveal.js framework](https://github.com/hakimel/reveal.js).

## Quickstart

```
git clone https://github.com/brainstorm/slides_ipfs_2016
npm install
npm start
```

## Generate PDF

The builtin reveal.js PDF converter does not work properly, therefore I would suggest using [decktape](https://github.com/astefanutti/decktape):

```
$ docker run --rm --net=host -v `pwd`:/slides astefanutti/decktape http://<ABOVE_NODEJS_INSTANCE_IP>:8000 slides.pdf
```
