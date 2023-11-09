
WARNING: This documentation is actively being developed and links may change.

# Getting Started

The Fuse Framework provides a means to build a native application with a webview user interface, without sacrificing the means to use device APIs from the webview.

This guide will go over how to setup the JavaScript environment and then will branch off into native environment. For plugin development, [click here](../plugin-development/getting-started.md).

For the purpose of this guide, we'll assume that you're starting off with an empty git repository.

## Requirements

To complete this guide you'll need:

- Current NodeJS LTS
- Webpack or another JS bundler

Additionally for Android development, Android Studio is required.

For iOS development, XCode will be required.

## The JS Runtime

Start off with creating a NPM package by issuing: `npm init`. Fill out the NPM prompt to create a NPM package.

(Optional) Once you're done, go into `package.json` and add `"private": true` to prevent accidentally publishing your app to NPM.

A quick note regarding the JS environment. While we are working with node modules, the JS environment ran inside the app is not a NodeJS runtime. Care has to be taken not to use NodeJS-specific modules.

Fuse framework makes use of TypeScript so it will make sense to also use TypeScript to get the advantage of compilation checks and some level of type safety. Fuse is also distributed as a CommonJS module, which means it can't be ran inside directly inside the webview as is. We require a web bundler. This guide will use Webpack but any bundler should do.

Let's start with installing our dependencies:

```
npm install --save-dev webpack webpack-cli typescript ts-loader source-map-loader @btfuse/core
```

WIP
