# AngularSixWorld

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.0.3.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

## New in Angular 6
### ng add
ng add @angular/pwa — Turn your application into a PWA by adding an app manifest and service worker
ng add @ng-bootstrap/schematics — Add ng-bootstrap to your application
ng add @angular/material — Install and setup Angular Material and theming and register new starter components into ng generate
ng add @clr/angular@next — Install and setup Clarity from VMWare
ng add @angular/elements — Add the needed document-register-element.js polyfill and dependencies for Angular Elements
### Material Data Table
$ ng generate @angular/material:material-table --name=my-table
### CLI v6 now has support for workspaces containing multiple projects, angular.json instead of .angular-cli.json
### Library Support
$ ng generate library my-lib - Generating a library
1. When you want to use a library from npm, you must:
- install the library into node_modules via npm install library-name
- import it in your application by name import { something } from 'library-name';
2. Using your own library follows a similar pattern:
- build the library via
$ ng build my-lib
- import it in your application by name
$ import { something } from 'my-lib';
3. Publishing your library
$ ng build my-lib --prod
$ cd dist/my-lib
$ npm publish
### Note for upgraded projects
1. If you are using an upgraded project, there are some additional changes you have to make to support monorepo (a workspace with multiple projects) setups:
- in angular.json, change the outputPath to dist/project-name for your app
- remove baseUrl in src/tsconfig.app.json and src/tsconfig.spec.json
- add "baseUrl": "./" in ./tsconfig.json
- change any absolute path imports in your app to be absolute from the root (including src/), or make them relative
2. This is necessary to support multiple projects in builds and in your editor. New projects come with this configuration by default.