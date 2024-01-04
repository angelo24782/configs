# Shared syncpack configuration

![](https://img.shields.io/npm/v/@clabnet/configs-syncpack.svg?color=brightgreen) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#)

The purpose of the [syncpack](https://www.npmjs.com/package/syncpack) is formatting package json and validating dependencies versions.

---

## Contents

- [Setup](#setup)
- [Usage](#usage)

## Setup

- Add workspace reference to `@clabnet/configs-syncpack` and its peer dependencies:

  ```sh
  pnpm add -w @clabnet/configs-syncpack syncpack
  ```

- Add syncpack configuration file:

  ```js
  // .syncpackrc.js

  module.exports = require('@clabnet/configs-syncpack')
  ```

- Add syncpack scripts:

  ```jsonc
  // package.json

  "scripts": {
    ...
    "syncpack:fix": "syncpack format && syncpack fix-mismatches"
    ...
  }
  ```

## Usage

- Manual usage from command line:

  ```sh
  pnpm format:check .
  pnpm format:fix .
  ```

---

[⬅ Back](../../README.md)

---
