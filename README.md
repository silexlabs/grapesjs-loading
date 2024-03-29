# Grapesjs Loading

Shows a loading bar while the site is loaded or saved. By default it looks like the classic loading bar on top of the page, e.g. on github.com.

> This demo is not useful as it uses localstorage as storage and this is instant so the loading bar is not visible => todo: make it better
[DEMO](https://codepen.io/lexoyo/full/GRYZBRN)
> This code is part of a bigger project: [about Silex v3](https://www.silexlabs.org/silex-v3-kickoff/)

### HTML
```html
<link href="https://unpkg.com/grapesjs/dist/css/grapes.min.css" rel="stylesheet">
<script src="https://unpkg.com/grapesjs"></script>
<script src="https://unpkg.com/@silexlabs/grapesjs-loading"></script>

<div id="gjs"></div>
```

### JS
```js
const editor = grapesjs.init({
	container: '#gjs',
  height: '100%',
  fromElement: true,
  storageManager: false,
  plugins: ['@silexlabs/grapesjs-loading'],
});
```

### CSS
```css
body, html {
  margin: 0;
  height: 100%;
}
```


## Summary

* Plugin name: `@silexlabs/grapesjs-loading`
* Shows a loading bar while the site is loaded or saved

## Options

| Option | Description | Default |
|-|-|-
| `option1` | Description option | `default value` |



## Download

* CDN
  * `https://unpkg.com/@silexlabs/grapesjs-loading`
* NPM
  * `npm i @silexlabs/grapesjs-loading`
* GIT
  * `git clone https://github.com/silexlabs/grapesjs-loading.git`



## Usage

Directly in the browser
```html
<link href="https://unpkg.com/grapesjs/dist/css/grapes.min.css" rel="stylesheet"/>
<script src="https://unpkg.com/grapesjs"></script>
<script src="path/to/@silexlabs/grapesjs-loading.min.js"></script>

<div id="gjs"></div>

<script type="text/javascript">
  var editor = grapesjs.init({
      container: '#gjs',
      // ...
      plugins: ['@silexlabs/grapesjs-loading'],
      pluginsOpts: {
        'grapesjs-loading': { /* options */ }
      }
  });
</script>
```

Modern javascript
```js
import grapesjs from 'grapesjs';
import plugin from '@silexlabs/grapesjs-loading';
import 'grapesjs/dist/css/grapes.min.css';

const editor = grapesjs.init({
  container : '#gjs',
  // ...
  plugins: [plugin],
  pluginsOpts: {
    [plugin]: { /* options */ }
  }
  // or
  plugins: [
    editor => plugin(editor, { /* options */ }),
  ],
});
```



## Development

Clone the repository

```sh
$ git clone https://github.com/silexlabs/grapesjs-loading.git
$ cd grapesjs-loading
```

Install dependencies

```sh
$ npm i
```

Start the dev server

```sh
$ npm start
```

Build the source

```sh
$ npm run build
```



## License

MIT
