# Web Services Setup

## Software Needed
#### Intercepting Proxy (choose at least 1) BurpSuite Pro would be the most ideal for the training
* [Download Burp Suite Community Edition - PortSwigger](https://portswigger.net/burp/communitydownload)
* [Request a free trial for Burp Suite Professional - PortSwigger](https://portswigger.net/requestfreetrial/pro) (If you want to a 30 day free trial of Burp Pro signup a few days before class because their process is not instant)
* Owasp Zap [Downloads · zaproxy/zaproxy Wiki · GitHub](https://github.com/zaproxy/zaproxy/wiki/Downloads)

#### Other
[SecLists](https://github.com/danielmiessler/SecLists)
```sh
git clone git@github.com:danielmiessler/SecLists.git
```

[LinkFinder: A python script that finds endpoints in JavaScript files](https://github.com/GerbenJavado/LinkFinder)

```sh
$ git clone https://github.com/GerbenJavado/LinkFinder.git
$ cd LinkFinder
$ python setup.py install
```

## Labs
We will have an AWS environment spun up for each lab but we cannot guarantee that it will be available. We have run into issues before where requests were blocked by the conference network to AWS. Therefore, we recommend running the labs locally. This will require Docker. 

Docker is the easiest way to run these labs but not the only way. 

### SOAP WebServices Lab

```sh
sudo docker run --rm -it -p 80:80 cyrivs89/web-dvws
```

https://github.com/snoopysecurity/dvws

### REST WebServices Lab

```sh
docker pull bkimminich/juice-shop
docker run --rm -p 3000:3000 bkimminich/juice-shop
```

### Graphql WebServices Lab
Requires Maven and Java 1.8
3 options to run locally

1. Use pre-built jar

[Download Jar](https://github.com/righettod/poc-graphql/releases)
```sh
java -jar graphql-poc.jar
```

2. Run from repo 
```sh
git clone git@github.com:righettod/poc-graphql.git
cd poc-graphql
mvn spring-boot:run
```
3. build your own jar
```sh
git clone git@github.com:righettod/poc-graphql.git
cd poc-graphql
mvn package
java -jar graphql-poc.jar
```

#### This is a 2 hour training so we don't have a lot of time to triage and help setup environments for everyone, please come prepared with these things already downloaded and running 
