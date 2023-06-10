# Modern JSDoc default template

Modern JSDoc default template with a Dark/Light theme style that closely resembles the Dark/Light theme found on GitHub

[![Run tests](https://github.com/dmh/modern-jsdoc-template/actions/workflows/test.yml/badge.svg)](https://github.com/dmh/modern-jsdoc-template/actions/workflows/test.yml)
![node-current](https://img.shields.io/node/v/modern-jsdoc-template)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
![JSDoc](https://img.shields.io/badge/API\%20documentation-JSDoc-yellow)

## [**Demo**](https://dmh.github.io/modern-jsdoc-template)

![screenshot](https://github.com/dmh/modern-jsdoc-template/assets/5150636/517a585d-7982-4e12-aa4c-e37f9037165f)

## Table of contents

- [Why?](#why)
- [Goal](#goal)
- [Features](#features)
- [Comparison Table](#comparison-table)
- [Quick start](#quick-start)
- [Contributing](#contributing)
- [Changelog](CHANGELOG.md)
- [Thanks](#thanks)

## Why?
**Dark/Light theme**

This template enhances the simple and minimalistic JSDoc default template by incorporating a dark and light theme styling, similar to GitHub's dark dimmed and light theme. There are no other significant alterations.

## Goal
**Minimal changes to the default theme.**

The JSDoc default theme has undergone minimal changes. The template only includes new styles and slight external script additions to the JSDoc default template. The main functionality and features remain unchanged. During the build process, most of the templates are copied from JSDoc without any modifications, ensuring alignment with the JSDoc default template in terms of features and functionality.

## Features:
- **Dark/Light theme** similar to GitHub light and dark dimmed themes
- [Highlight.js](https://github.com/highlightjs/highlight.js) as a code syntax highlighter instead of `prettify.js`
- Table of contents based on [tocbot.js](https://github.com/tscanlin/tocbot)
- [initial.css](https://www.npmjs.com/package/@resultify/initial.css) as a base root CSS styling

## Comparison Table
||JSDoc default template|Modern JSDoc template|
|---|---|---|
|**Publish Script**|`publish.js`|`publish.js` (_no changes, same as in JSDoc default template_)|
|**Code syntax highlighter script**|`prettify.js`(_self-hosted_)|`highlight.js` (_CDN_)|
|**Code line numbers script**|`linenumber.js` (_self-hosted_)|`highlightjs-line-numbers.js` (_CDN_)|
|**General CSS styling**|JSDoc default|**Dark/Light theme** (_similar to GitHub_)|
|**Code syntax highlighter styles**|JSDoc `prettify.js` theme|**Dark/Light theme** (_similar to GitHub_)|
|**Layout Template**|JSDoc default layout |JSDoc default layout with some modifications to add scripts and styles|
|**All others templates**|JSDoc default|Same as in **JSDoc default**, no changes!
|**Fonts**|OpenSans (_external_)|system fonts|
|**Table of contents**|no|yes|

## Quick start
1. Install `jsdoc`
```
npm install --save-dev jsdoc
```
2. Install `modern-jsdoc-template`
```
npm install --save-dev modern-jsdoc-template
```
3. Specify a source and template in `jsdoc.json`
```json
{
  "plugins": ["plugins/markdown"],
  "source": {
    "include": ["source???/"]
  },
  "templates": {
    "cleverLinks": true,
    "default": {
      "includeDate": false
    }
  },
  "opts": {
    "template": "node_modules/modern-jsdoc-template/default",
    "readme": "./README.md",
    "destination": "./docs/",
    "recurse": true,
    "verbose": true
  },
  "markdown": {
    "idInHeadings": true
  }
}
```
4. Generate documentation
```js
npx jsdoc -c jsdoc.json
```

## Contributing
1. Clone/fork the repository and run `npm install` to install dependencies.
2. Run `npm start` to start the development server with watcher.
3. Add your changes to `src/*` files and test the result in browser on `http://localhost:8082`
4. Run `npm test` to run tests.
5. Commit your changes and create a pull request.

## Thanks
- [JSDoc](https://jsdoc.app)
- [Highlight.js](https://github.com/highlightjs/highlight.js)
- [highlightjs-line-numbers.js](https://github.com/wcoder/highlightjs-line-numbers.js/)
- [Tocbot](https://github.com/tscanlin/tocbot)
- [GitHub dark/light theme](https://github.com)
- [initial.css](https://www.npmjs.com/package/@resultify/initial.css)
