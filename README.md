Reproduces a Prisma Miniflare 2 bug where displays the following error

> PrismaClient is unable to run in this browser environment, or has been bundled for the browser (running in `node`).

To trigger the error, run the tests in the Miniflare 2 environment

```
npm run itest
```


They pass when outside of the miniflare environment:

```
npm run itest-working
```


It looks like Cloudflare is working on Miniflare 3, but the testing story there is currently in development, and they recommend using Miniflare 2. Personally I tried migrating to Miniflare 3 and everything blew up in my face as soon as I tried something more involved (like setting up integration tests). It is not a simple migration so I gave up for the time being and I'm focusing on getting Miniflare 2 to work with Prisma.

Miniflare 3 page that recommends legacy: https://miniflare.dev/testing

Miniflare 2 testing docs: https://legacy.miniflare.dev/testing

