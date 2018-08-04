# jsdoc-polymer-plugin

Adds tags to help document polymer functionality without having to copy-paste text around and allowing disallowing undefined tags.  Most of these match up to the official polymer documention tags, but ported for jsdoc.

Install with:

```sh
yarn add --dev @zakkudo/jsdoc-polymer-plugin
```

Add to your jsdoc config with:

```js
    "plugins": [
        "@zakkudo/jsdoc-polymer-plugin"
    ],
```

Document your mixins like this this way:

```js
  /**
   * Add Application action creators to a polymer class.  It also connects the
   * component to the Redux store as well as manage any passed saga scripts.
   * @module Application/ActionsMixin
   * @polymer
   * @mixinFunction
   * @appliesMixin SagaMixin
   * @param {Polymer.PolymerElement} Parent - The class to mix into
   * @param {Function} saga - The saga to start with connection of the element to the DOM.
   * It will be stopped when disconnected.
   * @return {Polymer.PolymerElement} The wrapped class
   */
  export default (Parent, {actions, saga, store}) => {
```

Document your components like this

```js
/**
 * A toggle button which customizable label
 * @module lib/components/Toggle
 * @customElement
 * @polymer
 *
 */
```

Added tags include

- `@polymer`
- `@appliesMixin`
- `@customElement`
- `@mixinClass`
- `@mixinFunction`
- `@polymerBehavior`

Includes typedefs for

- `Polymer` namespace
- `Polymer.PolymerElement` typedef to describe a polymer class
