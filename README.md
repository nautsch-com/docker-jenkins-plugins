# jenkins plugins

docker image with a fix set of plugins for jenkins. The build is using

[hgomez's Scripted Jenkins Plugins install](https://gist.github.com/hgomez/2048146ddfb04ca42d91)

#### Usage:

Create a container based on this image and mount the container into
a container of the official [Jenkins](https://hub.docker.com/_/jenkins/) image:

    docker run --name jenkins-plugins nautsch/jenkins-plugins
    docker run -d --volumes-from jenkins-plugins jenkins

##### Change the plugins

Clone/fork the repo and change the content of the `excl-plugins.txt` and
`incl-plugins.txt` files. Use the name attribute from the plugin.
You can use the following URI to get all available plugins:

[http://updates.jenkins-ci.org/stable/update-center.json](http://updates.jenkins-ci.org/stable/update-center.json)

#### Tags:

* latest [(Dockerfile)](https://github.com/nautsch-com/docker-jenkins-plugins/blob/master/Dockerfile)