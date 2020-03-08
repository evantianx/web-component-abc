## Basic 

### `HTMLElement`

```js
document.createElement('div').constructor // f HTMLDivElement() { [native code] }

document.createElement('div').constructor.__proto__ // f HTMLELement() { [native code] }

document.createElement('randomelement').constructor // ƒ HTMLUnknownElement() { [native code] }

document.createElement('randomelement').constructor.__proto__ // f HTMLELement() { [native code] }

document.createELement('random-element').constructor // ƒ HTMLElement() { [native code] }
```

**Naming rules for Web Components:**

- There must be at least one dash(-) in your element name (like 'random-element' or 'random-' or 'random-element-1')

### define a customELement

```js
// handle collisions
if (!customELements.get('my-element')) {
  customELements.define('my-element', class extends HTMLELement {})
}
```