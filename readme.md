# Personal website

> Hello, future self.
>
> I'm documenting how to update and deploy this website in case you haven't
> done it in a while and forgot how to do it.
>
> Best,
>
> -- Past self

### Eleventy static-site generator

I'm using [eleventy](https://www.11ty.dev/) to generate a static site from markdown files. It's installed locally:

```
npm i --save-dev @11ty/eleventy
```

The eleventy command should always be invoked with `npx` like so:

```
npx @11ty/eleventy <command>
```

### Content sources and layouts

Raw content sources live in markdown files under the [`./content`](./content) directory.

Layouts go in [`./content/_includes`](./content/_includes) and are written in [nunjucks](https://mozilla.github.io/nunjucks/).

### Building

To build the site, navigate to the root directory and use eleventy:

```
npx @11ty/eleventy --input=./content
```

Output will go in the [`./_site`](./site) directory.

You can preview locally with the `--serve` option:

```
npx @11ty/eleventy --input=./content --serve
```

As long as a layout with a `<body>` tag is used, there's live preview.

### Hosting

I'm hosting this on [netlify](https://netlify.com).

### Click tacking

I'm using [cutt.ly](https://cutt.ly/) to track last 30 days of clicks on my links.
