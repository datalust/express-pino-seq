# Express + Pino + Pino-Seq

This is a example app created by using [`express-generator`](https://github.com/expressjs/express) and adding [`express-pino-logger`](https://github.com/pinojs/express-pino-logger) and [`pino-seq`](https://github.com/datalust/pino-seq) packages.

It's used to test end-to-end logging from a node.js app to [Seq](https://datalust.co/seq), using the [`pino`](https://github.com/pinojs/pino) logging library.

## Getting started

```
$ npm install
```

Make sure you have an instance of Seq running. The easiest way to do this is to run `docker run --name seq -d -e ACCEPT_EULA=Y -p 5341:80 datalust/seq:latest`

```
$ npm run start // pino-seq will send logs to localhost:5341 by default
```

Open [localhost:3000](http://localhost:3000) to browse your Express app, and generate request logs

Browse [localhost:5341](http://localhost:5341) to see your request logs in Seq.

Your request logs should look something like:
![Screenshot of Seq showing a log "request completed" from the Express app. Includes status code, headers, and response time](https://github.com/datalust/express-pino-seq/blob/dev/express-pino-seq-screenshot.png)