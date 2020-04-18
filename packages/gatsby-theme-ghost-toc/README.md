# gatsby-theme-ghost-toc
[![Released under MIT license.](https://badgen.net/github/license/micromatch/micromatch)](https://github.com/styxlab/gatsby-theme-ghost-toc/blob/master/LICENSE)
[![gatsby-theme-ghost-toc npm package version.](https://badgen.net/npm/v/gatsby-theme-ghost-toc)](https://www.npmjs.org/package/gatsby-theme-ghost-toc)
[![PRs welcome!](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)]()

Adds table of contents to posts. This theme makes use of component shadowing and showcases best practices for adding custom themes to `gatsby-theme-try-ghost`.

## Install

`yarn add gatsby-theme-ghost-toc`


## Dependencies

As this is an addon theme, installing [gatsby-theme-try-ghost](https://github.com/styxlab/gatsby-theme-try-ghost/tree/master/packages/gatsby-theme-try-ghost) is required. It's also required to install [gatsby-transformer-rehype](https://www.gatsbyjs.org/packages/gatsby-transformer-rehype/) as it provides the underlying table of contents data.

`yarn add gatsby-theme-try-ghost gatsby-transformer-rehype`

## How to use

```javascript
// In your gatsby-config.js
plugins: [
    {
        resolve: `gatsby-theme-ghost-toc`,
        options: {
            // Number of shown headline levels (optional, default: 2)
            maxDepth: 2,
        },
    },
]
```

> Make sure to include the plugins in the following order: gatsby-theme-try-ghost, gatsby-theme-dark-mode (if used), gatsby-transformer-rehype, gatsby-theme-ghost-toc.


## Details

This Gatsby theme plugin hooks into the `gatsby-theme-try-ghost` theme and adds a *table of contents* (Toc) box to posts. This plugin is responsible for the UI. On small screens, the ToC is placed directly under the feature image and before the main content. On large screens that are wider than 1170 pixels, the Toc is moved to the right hand side and is made sticky, so it can be used to navigate through the document.

The underlying ToC data is generated by gatsby-transformer-rehype, put into the GraphQL store and passed on to this plugin. See the [gatsby-transformer-rehype](https://www.gatsbyjs.org/packages/gatsby-transformer-rehype/) for further details.

The `maxDepth` option allows you to specify the number of headline levels shown. The maximum number is 6, but you'll most likely use 1 to 3. 


## Contributions

PRs are welcome! Consider contributing to this project if you are missing feature that is also useful for others. Explore [this guide](https://github.com/styxlab/gatsby-theme-try-ghost/tree/master/CONTRIBUTING.md), to get some more ideas.


# Copyright & License

Copyright (c) 2020 styxlab - Released under the [MIT license](LICENSE).