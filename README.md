# ASP.Net Core 2.2 and Vue.js 2.5.21 Template using vue-cli
>A web application template that abstracts the use of Webpack

## Scope of Project
This template project uses vue-cli-like configuration to build and run a web application with ASP.Net Core Web MVC backend.

## Prerequisits
You will need the following in order to run the template:
- Node.js v8.6.3+ and NPM v4+.
- The .Net Core 2.2 SDK.

## Installation
After extracting the core project files into a new root directory, run the following commands to build the necessary assets:
```sh
npm install
```
This installs the packages found in the `package.json` file.

Then use the `dontnet` command to build .Net Core dependencies:
```sh
dotnet restore
```
Or, if you are using Visual Studio, initiate a build in the project solution.

## Running a Local Server
To run our application locally, we need to use the node commands `npm run serve` or `npm run watch` (to edit changes on the fly).

In the root directory, run the following command:
```sh
npm run serve
```
This will start a local server for our application that we can preview.

However, if you want to edit the files directly without having to restart the local server, use the following command:
```sh
npm run watch
```
This allows the application to run locally and allow an automatic restart and build of the development environment every time there is a change or edit to the code/files.

## Production Build
To build a production ready minified output file, run the following:
```sh
npm run build
```
If successful, several new directories and files now should be located within the wwwroot\dist directory. 

The new `app.{random-hash}.js` file must be pointed in the Index.cshtml file under the Root View. Replace the source tag with the generated file within the Razor syntax of the scripts section
```sh
@sections Scripts {
    <script src="~/dist/js/app.js></script>
}
```

