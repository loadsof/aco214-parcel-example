# AC0214 - Parcel packager example

## About this repo

A quickstart repository with basic html, css and js files setup and ready for [ParcelJS](https://parceljs.org/) integration.

## Getting Started

1. Get your own copy of the repository

   - [Fork](https://docs.github.com/en/free-pro-team@latest/desktop/contributing-and-collaborating-using-github-desktop/cloning-and-forking-repositories-from-github-desktop#forking-repositories) this repository so that you have a copy in your own Github account
   - [Clone](https://docs.github.com/en/free-pro-team@latest/desktop/contributing-and-collaborating-using-github-desktop/cloning-and-forking-repositories-from-github-desktop#cloning-repositories) the repository from Github to your local development environment

2. Setup a project in VSCode either using the Projects+ extension, or simply selecting the _open in VS Code_ option for the repository in the Github Desktop app.

## Install the Parcel node module

1. Open the terminal in VS Code by either
   - Open the command palette with _cmd-shift-P_ and begin typing **Terminal** until you can see and select the _View: Toggle Terminal_ command; or
   - Select _Terminal_ from the _View_ menu; or
   - Use the **ctrl-`** (control and backtick) keyboard shortcut

# AC0214 - Parcel packager example

## About this repo

A quickstart repository with basic html, css and js files setup and ready for [ParcelJS](https://parceljs.org/) integration.

## Getting Started

1. Get your own copy of the repository

   - [Fork](https://docs.github.com/en/free-pro-team@latest/desktop/contributing-and-collaborating-using-github-desktop/cloning-and-forking-repositories-from-github-desktop#forking-repositories) this repository so that you have a copy in your own Github account
   - [Clone](https://docs.github.com/en/free-pro-team@latest/desktop/contributing-and-collaborating-using-github-desktop/cloning-and-forking-repositories-from-github-desktop#cloning-repositories) the repository from Github to your local development environment

2. Setup a project in VSCode either using the Projects+ extension, or simply selecting the _open in VS Code_ option for the repository in the Github Desktop app.

### Install the Parcel node module

1. Open the terminal in VS Code by either

   - Open the command palette with _cmd-shift-P_ and begin typing **Terminal** until you can see and select the _View: Toggle Terminal_ command; or
   - Select _Terminal_ from the _View_ menu; or
   - Use the **ctrl-`** (control and backtick) keyboard shortcut

2. In the terminal window type `npm install parcel-bundler` and wait for the package to download into your project folder

### Setup npm scripts

Open the `package.json` file. It should look something like this:

```JSON
{
  "name": "aco214-parcel-example",
  "version": "1.0.0",
  "description": "Example for setting up Parcel packager with a basic web project",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "aco214"
  ],
  "author": "Gil Fewster",
  "license": "ISC",
  "dependencies": {
    "parcel-bundler": "^1.12.4"
  }
}

```

You want to add two lines into the scripts section, above the test script which is already there:

```JSON
"watch":"parcel watch index.html",
"build":"parcel index.html",
```

After adding the new lines, your package.json file should look like this:

```JSON
{
  "name": "aco214-parcel-example",
  "version": "1.0.0",
  "description": "Example for setting up Parcel packager with a basic web project",
  "main": "index.js",
  "scripts": {
    "watch": "parcel watch index.html",
    "build": "parcel index.html",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "aco214"
  ],
  "author": "Gil Fewster",
  "license": "ISC",
  "dependencies": {
    "parcel-bundler": "^1.12.4"
  }
}

```

## Working with Parcel

You can now use the NPM scripts you set up in package.json to develop and build your code packages.

### - Development -

Open terminal from VS Code and enter `npm run watch`

This will start the Parcel bundler and development server. You stop the server, enter _ctrl-c_ in the terminal window.

When parcel is running in development mode, it prioritises build speed over optimisation, to ensure that the local server updates as quickly as possible. This means you can see your changes almost instantaneously.

### - Production -

Open terminal from VS Code and enter `npm run build`

This will create a bundle of code ready for deployment.

Development mode allows you to configure Parcel to generate more optimised, smaller files for deployment. These can take longer to generate, which is why we don't use a non-optimised mode for development.
