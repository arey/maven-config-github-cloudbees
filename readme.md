# Maven configuration for GitHub and CloudBees #

The primary goal of the [Maven configuration for GitHub and CloudBees](https://github.com/arey/maven-config-github-cloudbees) project is to provide a pom.xml and a  settings.xml examples both set up for working with GitHub as git remote repository and CloudBees as maven repository.

## Features ##

* Download artifacts from a maven repository hosted on the CloudBees forge
* Deploy artifacts to maven repository hosted on the CloudBees forge
* Release a project hosted on GitHub with the maven release plugin
* Hosting maven site under the cloudbees-forge release repository

## Getting Help ##

This readme file as well as the [wiki](https://github.com/arey/maven-config-github-cloudbeesswiki) are the best places to start learning about Hibernate Hydrate.

The [GitHub CloudBees Community](https://github.com/CloudBees-community) has already forked this project and thus could improve configuration files.

An [article published to the french blog Java & Moi](http://javaetmoi.com/2012/04/release-maven-windows-github-deploy-cloudbees/).


## Quick Start ##

* Fork the maven-config-github-cloudbees.git repository from GitHub
* Download the fork from GitHub: git clone git://github.com/<your github account>/<maven-config-github-cloudbees>.git
* Edit the pom.xml and change 
** SCM urls to your fork
** distributionManagement tags to your CloudBees private repository
** repositories tags to your CloudBees private repository
* Commit your changes then push them to GitHub
* Copy content of the settings.xml to your global or local maven settings.xml
* Change settings.xml cloudbees server credentials to your own
* Test the maven configuration file:
** mvn clean install
** mvn deploy
** mvn org.apache.maven.plugins:maven-scm-plugin:1.6:tag -Dtag=test -Dbasedir=.
** mvn release:prepare release:perform


## Contributing to Maven configuration for GitHub and CloudBees ##

* Github is for social coding platform: if you want to write code, we encourage contributions through pull requests from [forks of this repository](http://help.github.com/forking/). If you want to contribute code this way, please reference a GitHub ticket as well covering the specific issue you are addressing.


## Credits ##

* Uses [Maven](http://maven.apache.org/) as a build tool
* Uses [Cloudbees](http://www.cloudbees.com/foss) for continuous integration builds whenever code is pushed into GitHub
* Uses [GitHub](https://github.com/arey/maven-config-github-cloudbees) for hosting source code and documentation
