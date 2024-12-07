# Bygone Backend
By Niko Norwood

Basic NodeJS Library that adds some funtionality for basic web servers.

## Features
  * Unified console output with output logged in a TXT
  * Ability to cache a JS object using a JSON File (read to and from)

## Usage
Place bygone in your operating directory and import with `const bygone = require ('./bygoneBackend');`. Then instead of calling `console.log` you can call `bygone.output` or `bygone.debugOutput` and bygone will handle logging the output into a text file within the operating directory as well as console output. Bygone also supports caching and retriving a object in a JSON file with `new bygone.cachedFile(filepath)` which can save you the hassle of handling repeditive file IO.

## Examples
### Cached Object
 * `object = new bygone.cachedFile("file.json"); //sets file path and copies over contents into object.cache`
 * `object.updateCache(); //overwrites object with contents of file`
 * `object.updateFile(); //writes object to file`
### Output
 * `bygone.setDebug(true); //tells bygone to display outputs labeled as debug`
 * `bygone.output("console output");`
 * `bygone.debugOutput("hidden console output")`
