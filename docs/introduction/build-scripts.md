---
title: Build Scripts
description: Generating your stylesheet using build scripts.
date: 2021-01-03
---

## Build Scripts

Sass preprocessor is the only thing you need to get up and running. Uniform CSS comes with a predefined build commands in the `package.json`. The following **build commands** are available. By default, the following build scripts will automatically input `main.scss` and output files into the root directory. You can modify `package.json` to change the output location.

> Please note, if you are using the built-in build scripts or using the Sass CLI to compile, ensure the `--load-path` of your build command includes the `node_module/uniformcss/` path. For more information on load paths visit [Dart Sass Command Line Interface](https://sass-lang.com/documentation/cli/dart-sass#load-path).

{% include shortcodes/video, id: 'tLqqi5gyxQg' %}

---

### uniform

The following command will compile your Sass with `--style compressed` enabled. This is the command you should run when outputting for **production**.

```bash
yarn uniform
```

---

### uniform:compile

The following command will compile `styles.scss` and output `styles.css`.

```bash
yarn uniform:compile
```

---

### uniform:watch

The following command will compile `styles.scss` file and watch for changes.

```bash
yarn uniform:watch
```

---

### uniform:watch-compressed

The following command will compile `styles.scss` file and watch for changes with `--style compressed` enabled.

```bash
yarn uniform:watch-compressed
```

---

### uniform:purgecss

The following command will purge the output CSS based on the settings in `purgecss.config.js`. Make changes to `purgecss.config.js` to include all your markup template files and to ensure the correct amount of CSS is purged.

```bash
yarn uniform:purgecss
```

---

## Build Performance

Uniform CSS requires `dart-sass` version `1.33.0` and up. Using the Javascript version of Sass is slower than the stand-alone `dart` executable, therefore using the native `dart` version is recommended for fastest build time.