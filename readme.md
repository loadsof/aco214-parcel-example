# AC0214 - Parcel packager example

## About this repo

A quickstart repository with basic html, css and js files setup and ready for [ParcelJS](https://parceljs.org/) integration.

## Getting started

If you haven't already cloned the repo and set up Parcel, follow the instructions in [first-setup.md](first-setup.md).

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

## Things to notice

- Have a look at the `.gitignore` file. Gitignore intructs git to exclude specified files and directories from the repository. In this instance, we are excluding the node_modules, dist and .cache folder.
  - node_modules : this folder contains node packages from third party libraries installed with `npm install [x]` command. We don't want these in the repo, because npm installs them directly from their origin.
  - .cache : Parcel creates a cache folder with temporary files to speed up its build process. We don't need to keep this under source control.
  - dist : this is the folder which contains our generated website code. The code in this folder is what we deploy to our production web server... BUT we don't want to include it in source control, becuase it is generated from our ./src files when we run Parcel.
