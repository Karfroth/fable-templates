# Fable 2 Minimal App

**ATTENTION**: This template is not maintained anymore, please check [Getting Started in Fable docs](https://fable.io/docs/getting_started.html) for other ways to get started with Fable.

This is a simple Fable 2 app including an [Elmish](https://elmish.github.io/) counter with as little configuration as possible. If you want to see a more complex app including commonly used F# tools like Paket or Fake, check [the Fulma demo](https://github.com/MangelMaxime/fulma-demo).

## Requirements

* [dotnet SDK](https://www.microsoft.com/net/download/core) 2.0 or higher
* [node.js](https://nodejs.org) with [npm](https://www.npmjs.com/)
* An F# editor like Visual Studio, Visual Studio Code with [Ionide](http://ionide.io/) or [JetBrains Rider](https://www.jetbrains.com/rider/).

## Building and running the app

* Install JS dependencies: `npm install`
* Install F# dependencies: `dotnet restore src`
* Move to `src` directory to start Fable and Webpack dev server: `dotnet fable webpack-dev-server`
* After the first compilation is finished, in your browser open: http://localhost:8080/

Any modification you do to the F# code will be reflected in the web page after saving.

## Project structure

### npm

JS dependencies are declared in `package.json`, while `package-lock.json` is a lock file automatically generated.

### Webpack

[Webpack](https://webpack.js.org) is a JS bundler with extensions, like a static dev server that enables hot reloading on code changes. Fable interacts with Webpack through the `fable-loader`. Configuration for Webpack is defined in the `webpack.config.js` file. Note this sample only includes basic Webpack configuration for development mode, if you want to see a more comprehensive configuration check the [Fable webpack-config-template](https://github.com/fable-compiler/webpack-config-template/blob/master/webpack.config.js).

### F#

The sample only contains two F# files: the project (.fsproj) and a source file (.fs) in the `src` folder.

### Web assets

The `index.html` file and other assets like an icon can be found in the `public` folder.
