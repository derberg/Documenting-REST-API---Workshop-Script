This is a script for a workshop about documenting REST APIs.
This is a technical script that will be just a part of the workshop. It covers the setup of documentation portal but not the part where we learn about REST API

## Prerequisites

You need to have the following software/modules/applications installed on your computer to be able to complete all the steps of the workshop.

- Install Node.js and NPM: https://nodejs.org/en/download/ (both in one package) and then install:
 - [DocPad](http://docpad.org/) by calling in the terminal: `npm install -g npm`
 - [Gulp](http://gulpjs.com/) by calling in the terminal: `npm install -g gulp-cli`
- Get GitHub account: https://github.com/
- Install GitHub Desktop: https://desktop.github.com/
- Install some nice text editor like [Atom](https://atom.io/) or [Sublime Text](https://www.sublimetext.com/)

## Configuring documentation publishing pipeline

First you need to fork some projects and configure them correctly to set up the documentation independent generation pipeline.

1. Fork the following repos (it means open the links and click on Fork button in the top right corner of the page):
 - API Doc portal template: https://github.com/hybris/docpad-skeleton-apidocs
 - Sample REST API microservice that we will be documenting: https://github.com/derberg/minerva
 - Sample registry that integrates the template and docu sources: https://github.com/derberg/apidoc-workshop-docu_registry

2. Configuration
 - Modify `chewieConfig.js` file in forked `docpad-skeleton-apidocs` repository. Change the `path` attribute:
 ```
 path: process.env.REGISTRY_PATH || 'https://github.com/derberg/apidoc-workshop-docu_registry.git'
 ```
 The git url must point to your forked `apidoc-workshop-docu_registry` repository.

 - Modify `minerva.json` file in forked `apidoc-workshop-docu_registry` repository. Change the `location` attribute:
 ```
 "location": "https://github.com/derberg/minerva"
 ```
 The git url must point to your forked `minerva` repository.

## Start the API Doc portal locally

If configuration is completed you have to:

1. Clone your forked `docpad-skeleton-apidocs` repository
2. Navigate to its local clone in the terminal
3. Call the following command: `npm start`
4. Once the start is completed, open in the browser the following link: http://localhost:9778/

## Publishing to GitHub Pages

The easiest solution is to publish the API Doc portal on GitHub pages. Of course the generated API Doc portal files can be hosted on any other server as it is pure static content.

1. Create new repository with the following name: `your_github_username.github.io`. It must be public and initialized (You do it in UI during creation).
2. Modify `chewieConfig.js` file in forked `docpad-skeleton-apidocs` repository.
 - Change the `srcLocation` attribute:
 ```
 srcLocation: 'https://github.com/derberg/derberg.github.io.git',
 ```
 The git url must point to your newly created `your_github_username.github.io` repository.
 - Change the `docuUrl` attribute:
 ```
 docuUrl: process.env.docuURL || 'http://derberg.github.io',
 ```
 The page url must be the same as the name of your newly created `your_github_username.github.io` repository.
3. Modify `docpad.coffee` file in forked `docpad-skeleton-apidocs` repository. Change the `url` attribute:
```
environments:
  prod:
    templateData:
      site:
        url: "http://derberg.github.io"
```
It should point to the following url: `http://your_github_username.github.io`
4. Navigate to the local clone of `docpad-skeleton-apidocs` repository in the terminal
5. Call the following command: `npm run production`
6. Call the following command: `gulp pushResult`
7. Once the push is completed, open in the browser the following link: http://your_github_username.github.io
