# Safen

[![Downloads](https://img.shields.io/npm/dm/safen.svg)](https://npmcharts.com/compare/safen?minimal=true)
[![Version](https://img.shields.io/npm/v/safen.svg)](https://www.npmjs.com/package/safen)
[![License](https://img.shields.io/npm/l/safen.svg)](https://www.npmjs.com/package/safen)

[![NPM](https://nodei.co/npm/safen.png)](https://www.npmjs.com/package/safen)

Complex Object Validator Based on [lodash](https://github.com/lodash/lodash.js) and
[validator](https://github.com/chriso/validator.js) for TypeScript and JavaScript.

## Install

```
npm install safen --save
```

## Usage

Import,

```js
import * as safen from "safen"
// or
const safen = require("safen")
```

then,

@code("./test/readme.test.ts@usage-default", "typescript")


## Rule Examples

### Pipe

@code("./test/readme.test.ts@sample-pipe", "typescript")

### Optional

@code("./test/readme.test.ts@sample-optional", "typescript")

### Object in Object

@code("./test/readme.test.ts@sample-object-in-object", "typescript")

### Array

**Simple Array**

@code("./test/readme.test.ts@sample-simple-array", "typescript")

**Array With Range - Fixed**

@code("./test/readme.test.ts@sample-array-with-range-fixed", "typescript")

**Array With Range - Min**

@code("./test/readme.test.ts@sample-array-with-range-min", "typescript")

**Array With Range - Max**

@code("./test/readme.test.ts@sample-array-with-range-max", "typescript")

**Array With Range - Between**

@code("./test/readme.test.ts@sample-array-with-range-between", "typescript")

**Array with Multi Dimension**

@code("./test/readme.test.ts@sample-array-with-multi-dims", "typescript")

## Custom Error Messages

If needed, you can add custom error messages.

@code("./test/readme.test.ts@sample-custom-error-messages", "typescript")

The `:attribute` will be replaced by field name. For example :

@code("./test/readme.test.ts@sample-custom-error-messages-examples", "typescript")

## Validators

### Type

Validator                 | Description
------------------------- | -----------
**bool**                  | check if it is a `boolean`(alias to `boolean`).
**boolean**               | check if it is a `boolean`.
**float**                 | check if it is a `float`.
**int**                   | check if it is a `integer`(alias to `integer`).
**integer**               | check if it is a `integer`.
**number**                | check if it is a `number`.
**null**                  | check if it is a `null`.
**string**                | check if it is a `string`.
**symbol**                | check if it is a `symbol`.

Validator                 | Description | Example
------------------------- | ----------- | ------- |
**afte:{date = now}**     | check if the `string` is a date that's after the specified date. | `after`, `after:"2017-10-01"`, `after:"2017-10-01 14:30:00"`
**alpha**                 | check if the `string` contains only letters([a-zA-Z]). | `alpha`
**alphanum**              | check if the `string` contains only letters and numbers([a-zA-Z0-9]) | `alphanum`
**always_false**          | return always false, for debugging. | `always_false`
**always_true**           | return always true, for debugging. | `always_true`
**ascii**                 | check if the `string` contains only ascii characters. | `ascii`
**base64**                | check if the `string` is Base64. | `base64`
**before:{date = now}**   | check if the `string` is a date that's before the specified date. | `before:2017-10-01`, `before:2017-10-01 14:30:00`
**between:{min},{max}**   | check if the value(`string`, `number`) is between `{min}` and `{max}`. | `between:aaa,zzz`, `between:1,100`
**creditcard**            | check if the `string` is valid Credit Card number. cf. `0000-0000-0000-0000` | `creditcard`
**date**                  | check if the `string` is valid Date string(RFC2822, ISO8601). cf. `2018-12-25`, `12/25/2018`, `Dec 25, 2018` | `date`
**email**                 | check if the `string` is valid E-mail string. | `email`
**finite**                | check if the `number` is not `NaN`, `Infinity`, `-Infinity`. | `finite`
**hexcolor**              | check if the `string` is valid Hex Color string. cf. `#ffffff` | `hexcolor`
**in:{...params}**        | check if the value(`any`) is in an array `{params}`. | `in:1,2,3`, `in:safari,edge,firefox,"other browser"`
**ip:{version = all}**    | check if the `string` is valid UUID.<br />version is one of `all`(default), `v4`, and `v6`. | `ip`, `ip:v4`, `ip:v6`
**json**                  | check if the `string` is valid JSON. | `json`
**jwt**                   | check if the `string` is valid JWT. | `jwt`
**length:{size}**              | check if the value(`string`)'s length is `{size}`. | `length:16`
**length_between:{min},{max}** | check if the value(`string`)'s length is between `{min}` and `{max}`. | `length_between:4,20`
**length_max:{max}**           | check if the value(`string`)'s length is less than `{max}`. | `length_max:20`
**length_min:{min}**           | check if the value(`string`)'s length is greater than `{min}`. | `length_min:4`
**lowercase**             | check if the `string` is lowercase. | `lowercase`
**macaddress**            | check if the `string` is valid Mac Address. | `macaddress`
**max:{max}**             | check if the value(`string`, `number`) is less than {min}. | `max:5`
**min:{min}**             | check if the value(`string`, `number`) is greater than {max}. | `min:3`
**nan**                   | check if the value(`any`) is NaN. | `nan`
**port**                  | check if the `string` is valid PORT(0-65535). | `port`
**uppercase**             | check if the `string` is uppercase. | `uppercase`
**url**                   | check if the `string` is valid URL. | `url`
**uuid:{version = all}**  | check if the `string` is valid UUID.<br />version is one of `all`(default), `v3`, `v4`, and `v5`. | `uuid`, `uuid:v3`, `uuid:v4`, `uuid:v5`