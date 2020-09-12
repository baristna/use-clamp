# useClamp react hook

<a href="https://www.npmjs.com/package/use-clamp"><img alt="npm" src="https://img.shields.io/npm/v/use-clamp.svg"></a>

A <a href="https://reactjs.org/docs/hooks-intro.html">React Hook</a> to keep the given value(s) between the given minimum and maximum values.

<hr />

- <a href="#installation">Installation</a> <br/>
- <a href="#multiple-values">Multiple Values</a>

<hr/>

### Installation
```
$ yarn add use-clamp
```

Import
```js
import useClamp from 'use-clamp';
```

Usage
```js
const clampedValue = useClamp(value, 0, 100);
```

### Multiple Values
With passing array of numbers as first arguments will keep sum of the values between range.

 - Each value will stay above the min value.
 - If total of the values exceeds maximum value, each values will have the weighted values.

```js
const clampedValue = useClamp([20, 80, 50, 50], 0, 100);
// clampedValue = [10, 40, 25, 25]
```
