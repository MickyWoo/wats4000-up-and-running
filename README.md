# WATS 4000 - Example Vue.js App for Testing

> An example project for testing development environments.

This project asks you to set up your development environment, and then clone
this repository. Once you've cloned the repository, you will need to complete
the "Build Setup" below, and then you can run the development version of the
site on your local machine.

The goal here is to test your development environment to make sure it works
properly for the more complex work we will be doing later, and to start getting
an idea of what files and parts are included when we use `Vue-CLI` to
bootstrap a new project skeleton.

## Before You Begin

Be sure to set up your local development environment first. You can follow the
guidance in [Practical JavaScript 2: Building Applications](https://suwebdev.github.io/WATS-4000-gitbook/setting-up-workspace/) to get
started. Don't hesitate to supplement that resource with others specific to your
platform.

In order to run this project you will need an environment with the following:

* Working installation of Node.js
* Working installation of Git SCM
* Working setup for your Github account

## Basic Requirements
In order to successfully complete this project, fulfill the following
requirements.

* Set up your local development environment.
* Fork this repository into your own Github account.
* Clone this repository to your working development environment.
* Install dependencies by running `npm install` in the root of the repository.
* Test the site by running `npm run serve` to start the development server.
* Read through the site code and note the following:
    * What directories do you see? How do you interpret their names?
       > docs, node_modules,public, src, babel.config.js are all similar to original setup, but postcssrc.js is new and aliases.config.js
       > they all these names are all frameworks to me, preset data to build the website in the background hence .js /.json is my assumtion.

    * Where is the Vue app defined? (Which file?)
     > the vue app seems to be in the aliases.config because it points alias: require('./aliases.config').webpack

    * What is listed in `package.json`?
     > browserslist, postcss, eslintConfig, devDependencies, dependencies, besically an array listing all the broad items needed.

* Press `ctrl-c` in the terminal to exit the development server.
* Run `npm run build` and take a look at both the webpage that comes up and the output in the console.  
Consider the following questions:
    * what is in the node_modules directory?
        > they are the the parts and fucntions the come together to build your site.
    * where can you find the directions for the scripts run with `npm run`, that is the `serve` and `build` scripts 
       > -- grep -r "npm run"...bad idea gave me the whole list...
        but it found them under node-Modules 
        and README.md

    * what's the difference between the `dependencies` and `devDependencies` object in the package.json file?
        > it would seem like depensencies just rely on vue 2.5.21 and devDependencies rely on vue alongside bable and eslint, template complier.
        -- so its my assumtion that dependencies are the front page and devDependencie are the backend

    * Explore the `docs` directory. What do you see?
        > the docs contain:
        -assets which have the CSS and JS and Index.html. All of Which are the main structure of a webpage.

    * Do you see the filenames of the static files? What seems odd about those filenames?
        > when referring to just the Docs directory the static files seem to be all the css and .js files which are app.88 and chunk-vendors.  

    * Do you see the contents of your JS and CSS files? What has happened to those contents?
        > they are all pulling from webpacks and is not presented very nicely for coders is all I can say. And all use "sourceMapping"

    * Three config files have been supplied for you: `vue.config.js`, `aliases.config.js` and `.babel.config.js`. What is the general purpose of each file.  
        > vue.config.js : to me is funnel that directs all your items in "docs" which are assets > css and JS and HTML
        > aliases.config.js: directs all the information needed from webpacks
        > babel.config.js : directs all the information needed from vue and "presets" or I guess.

    * Describe (in words and with a flowchart/diagram) what happens when the `npm run build` command is executed to the best of your ability.  
        > I think `npm run build` command runs any of the items from the npm install which are the package.json files which are the rules(Vue.config.js) linking: src & node_modules and directories. 
        > THEN tempalates( babel./config.js) for your website. Which connect: "docs" that contain your CSS & .js

    * Make a diagram of the components of this system like the ones shown in the Practical JavaScript 2: Building Applications book `Types of Website Architectures`. Do your best to document your interpretation of the architecture of this system.
    
* Deploy your code to github.com and set up gh-pages on the `docs` directory.



## Stretch Goals
If you crave a challenge, attempt some of these goals.

* Modify some of the styles to present a nicer-looking app.
* Add a message that is populated with data from the Vue component (and output it into the template).
* Do some other fiddling with the logic to experiment and learn.

## Build Setup
The following commands will help you work with this project.

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run serve

# build for production with minification
npm run build

```

For detailed explanation on how Vue works, check out the [guide](https://cli.vuejs.org/guide/) and [docs for vue-loader](https://cli.vuejs.org/config/#css-loaderoptions).
