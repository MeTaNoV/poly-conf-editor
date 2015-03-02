# Introduction to poly-gen-conf-editor
This framework aims at developping a generic and dynamic configuration editor usable through configured Single Page Application  using Polymer (and Web Components) technologies.

# Description
PGCE should enable a user to simply instantiate a SPA and be able to create, modify, delete various set of configuration parameters.
The UI should be basically composed:
- a main area composed of several Tabs each enabling the edition of a given set of parameters conforming to one parameter definition
- Each tab should be composed of:
  - a side bar which contains a list of configuration parameters for a given definition
  - the main area which enable the edition of a given parameter
- on bottom, a tool bar to perform some actions like undo/redo/save/save all

A parameter definition should be the main element of configuration for a given set of UI elements represented in a Tab.
It could be a primitive value such as a String or integer or could represent complex structure. We will use the representation of Object in Javascript to define those parameter.

# Technical Discussion

- Which technic should be used to create dynamically the tab with regards to one parameter definition?
  - using HTML templates containing Web Components in a dynamic way?
  - creating dynamically for each definition Custom Components? (See http://w3c.github.io/webcomponents/spec/custom/). An unknown state could be maintained for temporary unregistered component which could be a solution...
- Mutation Observer to keep track of the history of modification for undo/redo features
- persistance choice: file/db

# Development Steps:

- create a first application that define 2 simple primitive parameter definitions (integer and string) and their associated edition tabs (parameters configuration will be still hard-coded and read-only)
- add the edition features to the tabs
- add the persistance features in mongoDB
- add the undo/redo mechanism
- transform the Tabs definition into a generic one
- add the possibility to add constraints to parameter values
- add the possibility to reference other parameter values
- add validate feature

# Installing the development environment
- Install node.js (get it here: http://nodejs.org/). This will additionally install npm, the node modules package manager
- Install bower which is a dedicated package manager for front-end application () thanks to npm
	- ```npm install -global bower```
- Initialize bower for our application using
	- ```bower init```
	- this will create a file called bower.json containing the properties of our application
- Install Polymer using bower
	- ```bower install --save Polymer/polymer```
	- this will create a bower_components directory containing the polymer component as well as all component it depends on (core-componentpage and webcomponentsjs in our case)
	- it also update the bower.json file to add the dependencies of our app to polymer
- 

