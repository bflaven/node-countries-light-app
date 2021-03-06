
## Node, API, Postman - Build a simple but complete REST API with Node, tested made with Chai and Newman, documented with Apidoc
A quick A to Z tutorial for non-developers who want to create a basic POC of an API with Node, Mongo. There is also explanations on how to add tests with Chai and a documentation with Apidoc.

[Read more on flaven.fr](http://flaven.fr/2018/05/node-api-postman-buid-a-simple-but-complete-rest-api-with-node-tested-with-chai-and-newman-documented-with-apidoc/)


### Requirements

If Homebrew, Node or Mongo are not installed. Here the shortest procedure to install all requirements on a Mac. Very brief but you got the essentials, if you have already installed these tools, you can jump to the point 1.

**Install Postman**<br />
[Check the website getpostman.com](https://www.getpostman.com/apps) - To manage the API, essential.

**Install Homebrew**<br />
[Check the website brew.sh](https://brew.sh/) or launch in the console the following command.

```
$ /usr/bin/ruby -e "$(curl -k -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

**Install Node and NPM**<br />

```
$ brew update
$ brew doctor
$ export PATH="/usr/local/bin:$PATH"
$ brew install node
```
Source: <a href="https://changelog.com/posts/install-node-js-with-homebrew-on-os-x" target="_blank">https://changelog.com/posts/install-node-js-with-homebrew-on-os-x</a>

**Install Newman globally**<br />
[Check the website brew.sh](https://brew.sh/) or launch in the console the following command.

```
  $ npm install -g newman
```
Source: <a href="https://support.getpostman.com/hc/en-us/articles/115003703325-How-do-I-install-Newman-" target="_blank">https://support.getpostman.com/hc/en-us/articles/115003703325-How-do-I-install-Newman-</a>


**Install MongoDB**<br />
```
$ brew update
$ brew install mongodb
```


At the root of your computer, create the default directory. 
```
  $ mkdir -p /data/db
```
<i>Run without specifying paths: If your system PATH variable includes the location of the mongod binary and if you use the default data directory (i.e., /data/db), simply enter mongod at the system prompt: <code>mongod</code></i>.


Source: <a href="https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/" target="_blank">https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/</a></li>


### Quick Presentation

You can read the article or not. Here is a quick presentation of the files contained in the repository and their usage.

**1. The directory tree**<br />
Here is the tree of the application that is contains in the directory **node-countries-light-app** 

See point 2 for the explanations of postman_files directory.

```
node-countries-light-app/
|-- _app
    |-- _controllers
        |-- countrie.controller.js
    |-- _models
        |-- countrie.model.js
    |-- _routes
        |-- countrie.routes.js
|-- _config
    |-- database.config.js
|-- postman_files
    |-- coll_node_countries_light_app.postman_collection.json
    |-- env_node_countries_light_app.postman_environment.json
|-- _node_modules
    |-- ... 
|-- _public
    |-- apidoc
        |-- ... 
|-- test
    |-- test_the_api.js
|-- apidoc.json
|-- package.json
|-- package-lock.json
|-- server.js

```

**2. JSON files for Postman**<br />
All the files used in Postman are in the directory **postman_files**. The files are stored in this directory, just for convenience. It has no use in the operation of the application.

Filename  | Description |
------------- | ------------- |
coll_node_countries_light_app.postman_collection.json | The collection of queries that can be imported in Postman. There are 6 queries for CRUD operations. 
env_node_countries_light_app.postman_environment.json  | The name for file environment that is imported in Postam under the name ENV_NODE_COUNTRIES_LIGHT_APP. The file contains the 2 variables {{api_root_url}} and {{api_root_url_countries}}

**3. More information**<br />
For those, who are looking for more information, a full article is available with additional resources is available @ [flaven.fr](http://flaven.fr/2018/05/node-api-postman-buid-a-simple-but-complete-rest-api-with-node-tested-with-chai-and-newman-documented-with-apidoc/)


### Clone this repository

For those who want to get the code directly, you can use the following command.

```
$ git clone https://github.com/bflaven/node-countries-light-app.git
$ cd node-countries-light-app
$ npm install

```

**After this, you can jump directly to the point 4. CREATE THE DB of the article** @ [flaven.fr](http://flaven.fr/2018/05/node-api-postman-buid-a-simple-but-complete-rest-api-with-node-tested-with-chai-and-newman-documented-with-apidoc/)















