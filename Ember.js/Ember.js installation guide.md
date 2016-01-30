# Ember.js installation Guide

1) Delete old version of nodejs, because there is no new versions of modules in current repository
     
    $ sudo apt-get remove nodejs nodejs-dev npm 
    
2) Install dependecies
     
    $ sudo apt-get install python-software-properties g++ curl libssl-dev apache2-utils ppa-purge
    
3) Add new repository and install npm (packet manager)
    
    $ sudo ppa-purge ppa:chris-lea/node.js
    $ sudo apt-get update
    $ sudo apt-get install nodejs nodejs-legacy nodejs-dev npm
    $ sudo npm install npm@latest -g
    
4) Set access to npm folder for current user
    
    $ sudo chown -R $USER ~/.npm
    $ sudo chown -R $USER /usr/local/lib/node_modules
    
5) Install nodejs last stable version
    
    $ sudo npm install -g n
    $ sudo n stable
    $ sudo npm cache clear    
    
6) Install ember.js, ember-cli and bower.
<VERSION is current node version, check it in folder or by command node -v (for example 5.4.0).
     
    $ sudo npm install -g ember-cli
    $ sudo ln -sf /usr/local/n/versions/node/<VERSION>/bin/node /usr/bin/node
    $ sudo npm install -g bower
