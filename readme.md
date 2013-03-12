# README

This is my Sass setup for new projects. It uses Sass and Compass to keep the CSS organised, less repetitive and easy to read. To use the CSS compiled into the /css folder, add the following to the `<head></head>` of your HTML page.

`<link rel="stylesheet" href="css/base.css">`

## Including Sass on the server

The /sass and /config folders (and their files) are not required on the server because the Sass is compiled locally.

## Editing Sass

Please avoid making any changes directly to base.css as these will be overwritten by the Sass in the /sass folder when compiled.

Please put any additional CSS into the /sass/scratch.scss file which will be pulled after every other Sass file (so should override the cascade where relevant) when compiled. Putting styles in this file also mean they can be refactored into the Sass at a later date. 

### Compiling Sass (and Compass)

You can compile Sass with many different tools. My preferred tool is [CodeKit](http://incident57.com/codekit/).

To add compile the files in this project using CodeKit, go to File > Add Project and navigate to the root folder containing these files. CodeKit will start 'watching' the relevant files. Whenever you save a file, CodeKit will compile all the files into the base.css stylesheet and you're good to go!

This project also uses Compass, a framework which provides pre-written rules for Sass. To add Compass to your CodeKit project, right-click on the project name in the Projects list and select Compass > Use Compass for this project. A dialog box will then pop up titled 'No configuration file'. A configuration file does exist, you just need to find it, so select the 'Locate' button in the dialog box. From there, navigate into the /config folder and select the config.rb file. Now you're done, Compass will be compiled when you next save the file.