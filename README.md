# Dummy Application

[![Apache License 2](https://img.shields.io/badge/license-ASF2-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0.txt)

## Table of Contents

- [Features](#installation)
- [Setup and Installation](#features)
- [API Documentation](#contributing)
- [FAQ](#faq)
- [License](#license)

## Features

This application Supports Following Features: 
* Create, Read, Update, Delete City ( Entity )
* Accepts a number, N, and returns a JSON array with the first N Fibonacci numbers
* Basic Hello world REST end point to get a 'Hello world' message.
* Simulate Deadlock situation.
* REST endpoint that accepts a JSON object containing a paragraph of text and returns a JSON array of objects in order. Also has the flexibility to set ascending or descendng order. Default is asc.
* A REST endpoint that queries an external REST service.
* View thread dump.
* View Metrcis.
* View Application health.
* Content Negotiation : User can request for either json or xml response.
* A Complete UI to test all API

## Technology Stack

* Spring
* Spring Boot
* HSQL
* Swagger
* Junit, Mockito
* JaCoCo
* JDK 1.8+

## Setup and Installation.

### Clone

- Clone this repo to your local machine using :  

### Setup

#### Run the Application with Maven plugin

> Go to root folder, open terminal and run following command

```shell
$ mvn clean install
```

> After then start the Aplication

```shell
$ mvn spring-boot:run

```
#### Run the Application with IDE
Import the maven prjoject on your IDE

```shell
Right click : Run as Maven clean
Right click : Run as Maven install
Right click : Run as Spring Boot App

```
`If Everything goes well, Application will be running on port 8080` and applcation root context will be : <a href="http://localhost:8080/DummyApp/">App</a>

## API Documentation

> The best way to test the API is through the swagger UI, click the Link below : 

<a href="http://localhost:8080/DummyApp/swagger-ui.html">Api Testing Page</a>

> When propmted for authetication provide 
```shell
user name : root
password : password
```
### Testing REQ [ 1 ] : "Hello World" REST endpoint

> On the UI hover over and click  "REQ [ 1 ] Hello World API : Hello World Resource" and 

> click on `GET` after then click on `Try it out!`

> Scroll Down to see the results.

`You can also try it with CURL`
```shell
curl -u root:password -X GET --header 'Accept: application/json' 'http://localhost:8080/DummyApp/hello/'
```
### Testing REQ [ 2 ] : Testing unique words and thier counts / frequencies.

> On the UI hover over and click  REQ [ 2 ] Frequency processing API and 

> click on `POST` 

> Here we have two parameters : 'sort' is defaulted to 'asc' . On the 'text' Text box supply your text 

> after then click on `Try it out!`

> Scroll Down to see the results.

`You can also try it with CURL`
```shell
curl -u root:password -X POST --header 'Accept: application/json' -d 'Test' 'http://localhost:8080/DummyApp/count'
```

### Testing REQ [ 3 ] : Returns a JSON array with the first N Fibonacci numbers.
> On the UI hover over and click  REQ [ 3 ] Number Utility API and 

> click on `POST` 

> on the fiboNumber text Box supply your number and

> after then click on `Try it out!`

> Scroll Down to see the results.

`You can also try it with CURL`
```shell
curl -u root:password  -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' 'http://localhost:8080/DummyApp/number/fibonacci/3'
```

## Testing REQ [ 4 ] : Endpoint that creates two threads that become deadlocked with each other.
> On the UI hover over and click  REQ [ 4 ] Consumer Producer API  and 

> after then click on `Try it out!`

> Scroll Down to see the results.

`You can also try it with CURL`

```shell
curl -u root:password -X GET --header 'Accept: application/json' 'http://localhost:8080/DummyApp/producerconsumer/'
```

## Testing REQ [ 6 ] : queries an external REST service using Spring RestTemplate.
> On the UI hover over and click  REQ [ 6 ] External API  and

> We have Three different APIs

>>/externaldata/
>>/externaldata/post/{id}
>>/externaldata/post/{userid}


**Badges will go here**

- build status
- issues (waffle.io maybe)
- devDependencies
- npm package
- coverage
- slack
- downloads
- gitter chat
- license
- etc.

[![Build Status](http://img.shields.io/travis/badges/badgerbadgerbadger.svg?style=flat-square)](https://travis-ci.org/badges/badgerbadgerbadger) [![Dependency Status](http://img.shields.io/gemnasium/badges/badgerbadgerbadger.svg?style=flat-square)](https://gemnasium.com/badges/badgerbadgerbadger) [![Coverage Status](http://img.shields.io/coveralls/badges/badgerbadgerbadger.svg?style=flat-square)](https://coveralls.io/r/badges/badgerbadgerbadger) [![Code Climate](http://img.shields.io/codeclimate/github/badges/badgerbadgerbadger.svg?style=flat-square)](https://codeclimate.com/github/badges/badgerbadgerbadger) [![Github Issues](http://githubbadges.herokuapp.com/badges/badgerbadgerbadger/issues.svg?style=flat-square)](https://github.com/badges/badgerbadgerbadger/issues) [![Pending Pull-Requests](http://githubbadges.herokuapp.com/badges/badgerbadgerbadger/pulls.svg?style=flat-square)](https://github.com/badges/badgerbadgerbadger/pulls) [![Gem Version](http://img.shields.io/gem/v/badgerbadgerbadger.svg?style=flat-square)](https://rubygems.org/gems/badgerbadgerbadger) [![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org) [![Badges](http://img.shields.io/:badges-9/9-ff6799.svg?style=flat-square)](https://github.com/badges/badgerbadgerbadger)

- For more on these wonderful ~~badgers~~ badges, refer to <a href="http://badges.github.io/badgerbadgerbadger/" target="_blank">`badgerbadgerbadger`</a>.

***INSERT ANOTHER GRAPHIC HERE***

[![INSERT YOUR GRAPHIC HERE](http://i.imgur.com/dt8AUb6.png)]()

- Most people will glance at your `README`, *maybe* star it, and leave
- Ergo, people should understand instantly what your project is about based on your repo

> Tips

- HAVE WHITE SPACE
- MAKE IT PRETTY
- GIFS ARE REALLY COOL

> GIF Tools

- Use <a href="http://recordit.co/" target="_blank">**Recordit**</a> to create quicks screencasts of your desktop and export them as `GIF`s.
- For terminal sessions, there's <a href="https://github.com/chjj/ttystudio" target="_blank">**ttystudio**</a> which also supports exporting `GIF`s.

**Recordit**

![Recordit GIF](http://g.recordit.co/iLN6A0vSD8.gif)

**ttystudio**

![ttystudio GIF](https://raw.githubusercontent.com/chjj/ttystudio/master/img/example.gif)

---

## Table of Contents (Optional)

> If you're `README` has a lot of info, section headers might be nice.

- [Installation](#installation)
- [Features](#features)
- [Contributing](#contributing)
- [Team](#team)
- [FAQ](#faq)
- [Support](#support)
- [License](#license)


---

## Example (Optional)

```javascript
// code away!

let generateProject = project => {
  let code = [];
  for (let js = 0; js < project.length; js++) {
    code.push(js);
  }
};
```

---

## Installation

- All the `code` required to get started
- Images of what it should look like

### Clone

- Clone this repo to your local machine using `https://github.com/fvcproductions/SOMEREPO`

### Setup

- If you want more syntax highlighting, format your code like this:

> update and install this package first

```shell
$ brew update
$ brew install fvcproductions
```

> now install npm and bower packages

```shell
$ npm install
$ bower install
```

- For all the possible languages that support syntax highlithing on GitHub (which is basically all of them), refer <a href="https://github.com/github/linguist/blob/master/lib/linguist/languages.yml" target="_blank">here</a>.

---

## Features
## Usage (Optional)
## Documentation (Optional)
## Tests (Optional)

- Going into more detail on code and technologies used
- I utilized this nifty <a href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet" target="_blank">Markdown Cheatsheet</a> for this sample `README`.

---

## Contributing

> To get started...

### Step 1

- **Option 1**
    - 🍴 Fork this repo!

- **Option 2**
    - 👯 Clone this repo to your local machine using `https://github.com/joanaz/HireDot2.git`

### Step 2

- **HACK AWAY!** 🔨🔨🔨

### Step 3

- 🔃 Create a new pull request using <a href="https://github.com/joanaz/HireDot2/compare/" target="_blank">`https://github.com/joanaz/HireDot2/compare/`</a>.

---

## Team

> Or Contributors/People

| <a href="http://fvcproductions.com" target="_blank">**FVCproductions**</a> | <a href="http://fvcproductions.com" target="_blank">**FVCproductions**</a> | <a href="http://fvcproductions.com" target="_blank">**FVCproductions**</a> |
| :---: |:---:| :---:|
| [![FVCproductions](https://avatars1.githubusercontent.com/u/4284691?v=3&s=200)](http://fvcproductions.com)    | [![FVCproductions](https://avatars1.githubusercontent.com/u/4284691?v=3&s=200)](http://fvcproductions.com) | [![FVCproductions](https://avatars1.githubusercontent.com/u/4284691?v=3&s=200)](http://fvcproductions.com)  |
| <a href="http://github.com/fvcproductions" target="_blank">`github.com/fvcproductions`</a> | <a href="http://github.com/fvcproductions" target="_blank">`github.com/fvcproductions`</a> | <a href="http://github.com/fvcproductions" target="_blank">`github.com/fvcproductions`</a> |

- You can just grab their GitHub profile image URL
- You should probably resize their picture using `?s=200` at the end of the image URL.

---

## FAQ

- **How do I do *specifically* so and so?**
    - No problem! Just do this.

---

## Support

Reach out to me at one of the following places!

- Website at <a href="http://fvcproductions.com" target="_blank">`fvcproductions.com`</a>
- Twitter at <a href="http://twitter.com/fvcproductions" target="_blank">`@fvcproductions`</a>
- Insert more social links here.

---

## Donations (Optional)

- You could include a <a href="https://cdn.rawgit.com/gratipay/gratipay-badge/2.3.0/dist/gratipay.png" target="_blank">Gratipay</a> link as well.

[![Support via Gratipay](https://cdn.rawgit.com/gratipay/gratipay-badge/2.3.0/dist/gratipay.png)](https://gratipay.com/fvcproductions/)


---

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2015 © <a href="http://fvcproductions.com" target="_blank">FVCproductions</a>.
