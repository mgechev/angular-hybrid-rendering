# Deprecated

Angular Universal 11.1 now has native hybrid rendering support. All you need is run `yarn prerender` and start the server `node dist/.../server/main.js`, from there Universal will take care of the rest. Find an example [here](https://github.com/mgechev/hybrid-rendering).

# Hybrid rendering

This application performs prerendering (a.k.a. server-side generation or SSG) for static routes and server-side rendering (SSR) for dynamic routes.

## How to use?

```bash
npm i
ng run todo:prerender
node dist/todo/server/main.js
```

## How it works?

*This requires almost zero changes in the default setup*

At build time, Angular Universal discovers all the routes declared in the application by statically analyzing the source code. After that, it prerenders all the routes without parameters.

The server verifies if a given requested path is already prerendered, and if so, it directly returns the static content. Alternatively, it delegates rendering to Universal.

## License

MIT

