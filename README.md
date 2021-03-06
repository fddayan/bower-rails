bower-rails
===========

rake tasks for bower on rails. Dependency file is bower.json in Rails root dir.

**Requirements**

* [node](http://nodejs.org) ([on github](https://github.com/joyent/node))
* [bower](https://github.com/twitter/bow) installed with npm

**Install**

in Gemfile

``` Ruby
	gem "bower-rails", "~> 0.2.1"
```

**Initialize**

To add an empty bower.json file to the project root.

``` Bash
	rails g bower_rails:initialize
```


**Configuration**

The bower.json file is two seperate bower [component.js](https://github.com/twitter/bower#defining-a-package) files. Defining a package in lib and vendor will install those packages to the corresponding directories.

**example bower.json file**

``` javascript
{
   "lib": {
    "dependencies": {
      "threex"      : "git@github.com:rharriso/threex.git",
      "gsvpano.js"  : "https://github.com/rharriso/GSVPano.js/blob/master/src/GSVPano.js"  
    }    
  },
  "vendor": {
    "dependencies": {
      "three.js"  : "https://raw.github.com/mrdoob/three.js/master/build/three.js"
    }
  }
}
```


**Available commands**

``` bash
  rake bower:install #install js components
  rake bower:update  #update js components
```
