# Is Primitive (JavaScript)

[**⚖️** MIT](./LICENSE.md)

**🗂️**
[![GitHub: hugoalh-studio/is-primitive-js](https://img.shields.io/badge/hugoalh--studio/is--primitive--js-181717?logo=github&logoColor=ffffff&style=flat "GitHub: hugoalh-studio/is-primitive-js")](https://github.com/hugoalh-studio/is-primitive-js)
[![NPM: @hugoalh/is-primitive](https://img.shields.io/badge/@hugoalh/is--primitive-CB3837?logo=npm&logoColor=ffffff&style=flat "NPM: @hugoalh/is-primitive")](https://www.npmjs.com/package/@hugoalh/is-primitive)

**🆙** ![Latest Release Version](https://img.shields.io/github/release/hugoalh-studio/is-primitive-js?sort=semver&color=2187C0&label=&style=flat "Latest Release Version") (![Latest Release Date](https://img.shields.io/github/release-date/hugoalh-studio/is-primitive-js?color=2187C0&label=&style=flat "Latest Release Date"))

A JavaScript module to determine whether the item is a primitive.

## 🎯 Target

- Bun ^ v1.0.0
- Cloudflare Workers
- Deno >= v1.34.0
  > **🛡️ Require Permission**
  >
  > *N/A*
- NodeJS >= v16.13.0

## 🔰 Usage

### Via Installation

> **🎯 Supported Target**
>
> - Cloudflare Workers
> - NodeJS

1. Install via console/shell/terminal:
    - Via NPM
      ```sh
      npm install @hugoalh/is-primitive[@<Tag>]
      ```
    - Via PNPM
      ```sh
      pnpm add @hugoalh/is-primitive[@<Tag>]
      ```
    - Via Yarn
      ```sh
      yarn add @hugoalh/is-primitive[@<Tag>]
      ```
2. Import at the script (`<ScriptName>.js`):
    ```js
    import ... from "@hugoalh/is-primitive";
    ```
    > **ℹ️ Note**
    >
    > Although it is recommended to import the entire module, it is also able to import part of the module with sub path if available, please visit [file `package.json`](./package.json) property `exports` for available sub paths.

### Via NPM Specifier

> **🎯 Supported Target**
>
> - Bun
> - Deno

1. Import at the script (`<ScriptName>.js`):
    ```js
    import ... from "npm:@hugoalh/is-primitive[@<Tag>]";
    ```
    > **ℹ️ Note**
    >
    > Although it is recommended to import the entire module, it is also able to import part of the module with sub path if available, please visit [file `package.json`](./package.json) property `exports` for available sub paths.

## 🧩 API

- ```ts
  function isPrimitive(item: unknown): item is Primitive;
  ```
- ```ts
  type Primitive = bigint | boolean | number | string | symbol | null | undefined;
  ```

## ✍️ Example

- ```js
  isPrimitive({});
  //=> false
  ```
- ```js
  isPrimitive(new Headers());
  //=> false
  ```
- ```js
  isPrimitive(true);
  //=> true
  ```
- ```js
  isPrimitive(123n);
  //=> true
  ```
