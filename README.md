# docker-centos-nodejs
Dockerfile for building a container for local nodejs-based api development.

The container has Node, npm, grunt-cli, and bower installed that automatically runs the following commands:

$ npm install

$ node app.js

Intended to be executed from a directory with an app.js file with the following command:

$ docker run –privileged=true -it -p 3000:3000 -v $(pwd):/var/www thompsa6/docker-centos-nodejs

Notes:

Will be visible on the docker host port 3000 (for MacOS, use 'boot2docker ip')
