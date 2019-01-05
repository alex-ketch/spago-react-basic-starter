# react-basic-starter (Spago fork)

This is a fork of
[justinwoo/spacchetti-react-basic-starter](https://github.com/justinwoo/spacchetti-react-basic-starter),
which is in turn a fork of [LumiHQ/React-Basic-Starter](https://github.com/lumihq/react-basic-starter).

## Requirements

- [Purescript](http://www.purescript.org): A strongly-typed functional programming language that compiles to JavaScript
- [Spago](https://github.com/spacchetti/spago): PureScript package manager and build tool

## Quickstart

```sh
git clone git@github.com:alex-ketch/spago-react-basic-starter.git
cd spago-react-basic-starter
spago install
npm install
npm run dev
```

## Development

```sh
npm run dev
```

This will run Parcel in watch mode, and provides Hot-Reloading for the app
whenever the PureScript sources change. However you still have to build the
PureScript sources by yourself, either through the [IDE PureScript plugin](https://github.com/nwolverson/atom-ide-purescript)
or running `spago build` after making and saving your changes.

## Production Build

This will use [Parcel](https://parceljs.org) to output an optimized files to the `/dist` directory.

```sh
npm run build
```

## Compatability with [IDE PureScript plugin](https://github.com/nwolverson/atom-ide-purescript)

As outlined in [this Spago issue](https://github.com/spacchetti/spago/issues/63#issuecomment-450750868),
IDE Purescript plugin by default expects packages to be installed by Bower os
psc-package.

For full compatibility, including auto-building your project, please update
the IDE Purescript plugin settings to:

```json
"purescript.buildCommand": "spago build -- --json-errors",
"purescript.packagePath": ".spago/*/*/src/**/*.purs"
```
