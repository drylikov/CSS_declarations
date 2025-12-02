




# CSS declarations







Parse and stringify CSS declarations (such as the HTML `style` attribute).





## Install





This package is ESM only: Node 12+ is needed to use it and it must be `import`ed
instead of `require`d.

[npm][]:

```sh
npm install css-declarations
```





## Use





```js
import {parse, stringify} from 'css_declarations'

var values = parse(`
  color:/*red*/purple;
  -webkit-border-radius: 3px !important;;
`)
// => {color: 'purple', webkitBorderRadius: '3px !important'}

stringify(values)
// => 'color: purple; -webkit-border-radius: 3px !important;'
```





## API





This package exports the following identifiers: `parse`, `stringify`.
There is no default export.

### `parse(value[, options])`

Parse CSS declarations from `string` to `object`.

###### `options.warning`

When given, `warning` is called when an error is encountered
([`Function`][warning]).


###### Returns

`Object.<string>` — Declarations.

### `stringify(values)`

Serialize CSS declarations from `object` to `string`.

###### Returns

`string` — Serialized declarations.

### `function warning(reason, offset)`

Invoked when an error occurs.
Errors come from [`reworkcss/css`][css].

###### Parameters

*   `reason` (`string`) — English reason for error;
*   `offset` (`number`) — Index-based position of error.

<!-- Definitions -->

[build]: https://github.com/drylikov/css_declarations/actions

[coverage-badge]: https://img.shields.io/codecov/c/github/drylikov/css_declarations.svg

[coverage]: https://codecov.io/github/drylikov/css_declarations

[downloads-badge]: https://img.shields.io/npm/dm/css_declarations.svg

[downloads]: https://www.npmjs.com/package/css_declarations

[size-badge]: https://img.shields.io/bundlephobia/minzip/css_declarations.svg

[size]: https://bundlephobia.com/result?p=css_declarations

[npm]: https://docs.npmjs.com/cli/install

[warning]: #function-warningreason-offset

[css]: https://github.com/reworkcss/css




