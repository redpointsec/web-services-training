# REST Services Walkthrough Exercises

### Description
Find REST endpoints, fuzz endpoints. 

## Tools

[LinkFinder: A python script that finds endpoints in JavaScript files](https://github.com/GerbenJavado/LinkFinder)

[Sqlmap Download](https://github.com/sqlmapproject/sqlmap/zipball/master)

```
brew install sqlmap
```

## Walkthroughs

| Attack Type | Application | Location | Tool |
| ---- | ---- | ---- | ---- |
| Find REST API Endpoints | JuiceShop | http://juicshop:80/main.js |  Linkfinder |
|Find Swagger| Altoro | [Altoro]()https://demo.testfire.net)| Linkfinder |

### Find REST API Endpoints

1. Open Juice Shop and intercept traffic with proxy
2. Look in the proxy for the main.js file and copy url to file

![find-js-file.png](:storage/2ff271b5-9a1d-4110-bb69-53d1dbe3a8dc/5f34f8ec.png)

3. Open terminal and run linkfinder with copied url
```sh
$ python3 linkfinder.py -i "http://3.17.173.103/main.js"
```
4. Findings will open in browser

![LinkFinder-output.png](:storage/2ff271b5-9a1d-4110-bb69-53d1dbe3a8dc/8eeaea68.png)


### Find Swagger
1. Use Google Dorks
```sh 
site:demo.testfire.net inurl:swagger
```
![google-swagger.png](:storage/2ff271b5-9a1d-4110-bb69-53d1dbe3a8dc/1cbf592a.png)

![altoro-swagger.png](:storage/2ff271b5-9a1d-4110-bb69-53d1dbe3a8dc/6f53f58f.png)


| Challenge | Difficulty |
| ----- | ----- |
| Juice Shop |http://3.17.173.103/#/|
| Find  App Configuration | :star: |
| SQL Injection | :star::star: | 
| Look in another users basket | :star::star: | 
| Altoro jsmith:demo1234 | http://demo.testfire.net/swagger/index.html#/|
| Insecure Direct Object Reference | :star::star: |





