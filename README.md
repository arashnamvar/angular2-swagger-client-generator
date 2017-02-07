# Whats new in this fork?
* Parsing YAML file instead of JSON
* Fixed duplicit imports when a required sub-model is used multiple times
* Generating dummy constructors instead of plain objects
* Using Handlebars instead of Mustache
* After all, I disabled the service generator alltogether as
  we have to handle way too many special cases on our own.

# Installing
Just install it using
`npm i -g kub1x/angular2-swagger-apiclient-generator`
and use it with:
`npm run cleangen && npm run apigen`
where (in `package.json` file):
```
"cleangen": "npm run rimraf -- src/app/apigen",
"apigen": "a2apigen -s swagger.yaml -o src/app/apigen"
```

# ORIGINAL DOCUMENTATION: angular2-swagger-apiclient-generator
Angular 2 API client generator from swagger json

# Description
This package generates a angular2 typescript class from a swagger v2.0 specification file. The code is generated using mustache templates.

# How to get it working

## Installation
1. `npm install angular2-swagger-client-generator`

or

1. get it from github `git clone https://github.com/nvdnkpr/angular2-swagger-client-generator`
1. `cd angular2-swagger-client-generator`
1. `npm install`
1. `npm run build`

## Usage

From commandline run:
```
a2apigen -s [yopur/path/to/swagger.json]
```

or
```
a2apigen -u [url/of/your/swagger.json]
```

## Example usage:

This command will generate API client described in swagger.json file to ./out folder
```
a2apigen -s .\tests\apis\swagger.json -o ./out
```

or from repository directory run:
```
node ./src/main -s .\tests\apis\swagger.json -o ./out
```

##Note:
This project was inspired by:

[swagger-js-codegen](https://github.com/wcandillon/swagger-js-codegen) project

