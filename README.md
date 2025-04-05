# stitches-babel-plugin

## Input

```js
let foo = styled('div', {});
```

## Output

```js
let foo = styled.withConfig({ displayName: 'foo' })('div', {});
```

## Installation

1. Install packages
```sh
$ npm install @stitches/react@1.3.1-1 stitches-babel-plugin
```

2. Extend babelrc
**.babelrc**

```json
{
  "plugins": ["stitches"]
}
```

3. Use createStitches
```tsx
import { createStitches } from "@stitches/react";

// Using createStitches is required!!!
const { styled } = createStitches(); 

const StyledForm = styled("form", {
  background: "red",
});
```



## Acknowledgements

This plugin is adapted from [@babel/plugin-transform-react-display-name](https://github.com/babel/babel/tree/main/packages/babel-plugin-transform-react-display-name) many thanks to the Babel team.
