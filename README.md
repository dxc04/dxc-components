# @datay/dxc-components  [![npm version](https://badge.fury.io/js/%40datay%2Fdxc-components.svg)](https://badge.fury.io/js/%40datay%2Fdxc-components) 

> Sample setup for creating vue lib and web component

## Usage

Within node environment
```sh
$ npm install --save @datay/dxc-components
```

```js
<script>
import { Button, AnotherButton } from "@datay/dxc-components"

export default {
    components: {
        Button,
        AnotherButton
    }    
}
</script>

<template>
    <div>
        <Button />
        <AnotherBUtton />
    </div>
</template>
```
or on existing non vue project

```html
<script src="https://unpkg.com/vue"></script>
<script src="https://unpkg.com/@datay/dxc-components"></script>
<div id="app">
    <dxc-components-button />
</div>
```

## Building Components

Make sure first that vue cli and vue cli-service-global was installed globally.
They will be use on building packages and service components
```sh
npm install -g @vue/cli @vue/cli-service-global
```

To build for lib and web components
```sh
npm run build
```

To only build lib components
```sh
npm run build:lib
```

To only build web components
```sh
npm run build:wc
```

## Working on Components
When working on the components, there are too ways to vuew the output: 
- via script tag -> wc
- via serving the vue component -> lib


### Web Components
- Before the changes are reflected, make sure to build your changes.
```sh
npm run build:wc
```
- Load demo html in `./dist/demo.html` to your browser

### Lib Components
- Serve vue component
```sh
vue serve src/components/Button.vue
```
- See component in action on http://localhost:8080

## License

MIT © [Dixie Philamerah Atay](https://github.com/dxc04)

