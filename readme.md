# Smarterliving Itactica_Intenso Theme

This is the main [Smarterliving](http://shop.smarterliving.nl) Magento 1.9.x.x Theme [Itactica Intenso](https://www.getintenso.com) is a third party Magento theme based on Zurb Foundation 5.5 that is modified to suit the specific needs for Smarterliving.

It consists of the following folders:

-  **Archive** - This is where all versions of the original theme files are archived, including the *current version*. In each version you'll find the following specific folders:
  - PSD Files - All Photoshop sources for Intenso theme
  - Theme Files - The actual Magento Theme files
-  **Smarterliving** - The ROOT folder for development and deployment. Contains the *current version*, and Smarterliving specific modifications.
  - assets - Contains source files of the *current version* of Intenso and Smarterliving specific modifications, magento modules, .phtml files etc.
  - bower_components - contains components pulled in using bower
  - **dist** - Contains the complete itactica_intenso/smarterliving theme, built from assets/bower_components/src, using [brunch](http://brunch.io/).
  - src - contains SCSS/SASS sources, theme translation sources and color schemes

## Changelog
A Changelog is kept in [changelog.md](changelog.md)

## How to get up and running on a Mac
This assumes [brew](http://brew.sh) -- the missing package manager for MacOS -- is already installed.

1. Install [NPM/Node.JS](nodejs.org); Preferably via [brew](http://brew.sh) [brew install node]; NPM is a Javascript/node.js package manager
2. Install [Brunch.io](http://brunch.io); Preferably via npm [npm install -g brunch]; Brunch is the Build Tool
3. Install updated version of rsync for mac via [brew](http://brew.sh) [brew install rsync]; this updated rsync is used to deploy to the dev-server
4. Install [terminal-notifier](https://github.com/julienXX/terminal-notifier); Preferably via [brew](http://brew.sh) [brew install terminal-notifier]; This notifies you once the files are uploaded to the dev-server.
5. Install [gawk](https://www.gnu.org/software/gawk/); Preferably via [brew](http://brew.sh) [brew install gawk]; compiles the language translations files

## How to do development?
All development to itactica_intenso is done on the local machine. [Brunch.io](http://brunch.io) is the build tool that assembles all assets in the "dist" folder and -during active development- uploads these to the development server, using the afterBrunch.sh script.

Brunch is started via the terminal in the Smarterliving folder:
- Build once with: [brunch build]
- Use [brunch watch] to build on save
