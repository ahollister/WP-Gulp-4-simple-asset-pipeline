# WP - Gulp 4 simple asset pipeline
A gulpfile.js and associated package.json for use in WordPress projects, (although it can easily be used independently of WP, just plug desired src and dest directories into the config object). 

Uses Gulp 4 and processes SCSS and JS into minified, concatenated files, with support for globbed SCSS imports, CSS autoprefixing, Babel preset-env, sourcemaps, BrowserSync, and a watch task. 

Gulp 4 includes support for parallel tasks, so it's quick since it can process SCSS and JS asynchronously.

## Prerequisites
Requires that you have 'gulp-cli' installed globally, if you are still using the 'gulp' package globally and haven't updated to gulp-cli, you'll need to remove that and install gulp-cli instead.

## Installation
1. Drop the contents of this repository into your WordPress theme.
2. Run `npm install` in your theme directory to install dependancies.
3. Edit the config object in gulpfile.js to match your desired input files and destinations for the processed files.

That's it!

## Configuration
The config object allows you to set the following values for __SCSS__:
`src` - The source file for compilation that contains your final import statements, should import everything that you want in the final file.
`srcDir` - The directory which contains all your SCSS files, this is the dir that the watch task watches for file changes to recompile automatically.
`dest` - The directory where you want your final CSS file to end up.

The config object allows you to set the following values for __JavaScript__:
`src` - The source file/files which gulp will process and watch for changes.
`dest` - The directory where you want your processed JS file to end up.

The config object allows you to set the following values for __BrowserSync__:
`active` - Determines whether BrowserSync will run, true or false, false by default.
`localURL` - This has to match the URL you are viewing the local site with, .
