# README

This is my Sass setup for new projects. It uses Sass and Bourbon.io to keep the CSS organised, less repetitive and easy to read. To use the CSS compiled into the /css folder, add the following to the `<head></head>` of your HTML page.

`<link rel="stylesheet" href="css/base.css">`

## Including Sass on the server

The /sass folder (and its files) are not required on the server because the Sass is compiled locally.

## Editing Sass

Please avoid making any changes directly to base.css as these will be overwritten by the Sass in the /sass folder when compiled.

Please put any additional CSS into the /sass/scratch.scss file which will be pulled after every other Sass file (so should override the cascade where relevant) when compiled. Putting styles in this file also mean they can be refactored into the Sass at a later date. 

### Compiling Sass (and Bourbon.io)

You can compile Sass with many different tools. My preferred tool is [CodeKit](http://incident57.com/codekit/).

To add compile the files in this project using CodeKit, go to File > Add Project and navigate to the root folder containing these files. CodeKit will start 'watching' the relevant files. Whenever you save a file, CodeKit will compile all the files into the base.css stylesheet and you're good to go!

This project also uses Bourbon.io, a framework which provides pre-written rules for Sass. To add Bourbon.io to your CodeKit project, right-click on the project name in the Projects list and select Bourbon > Use Bourbon for this project. Now you're done, Bourbon will be compiled when you next save the file.

If you use these files directly, CodeKit will recognise that Bourbon is included with no further actions required.

## A little word on submodules

I don't recommend including this as a Git submodule, it's more of a framework. The mixins file in itself might work as a submodule, but if you use the lot as a submodule, you won't be able to commit any further changes you make to the files. (Not ideal, as these are made to be built upon.) Previously, I didn't understand that this was how submodules worked, so I include this as a warning for anyone else who makes that same assumption!