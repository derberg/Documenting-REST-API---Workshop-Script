## REST API -> The easiest and coolest docu to write

This is a script for a workshop about documenting REST APIs. The workshop covers two aspects:
- Learning what REST API is,
- Setting up a portal with REST API documentation.

## Intro

REST API in most cases is used in the cloud environment. If you are documenting REST API for cloud - you are lucky because:
- You most likely have not only production but also stage environment set up permanently. This means you have a playground where you can check the API before you document it:
```
Like for the sake of this workshop we have a real service running.
Just navigate to this link in the browser:
 http://minerva.us-west-2.elasticbeanstalk.com/events
```
- In cloud all the peaces are independent and super easy to set up locally.
```
Minerva service mentioned above is also easy to set up locally. Just follow below steps in the terminal:
> git clone https://github.com/derberg/minerva.git
> cd minerva
> npm install
> npm run develop
```
- REST is easy to learn.
```
Again navigate in the browser to the Minerva service:
http://minerva.us-west-2.elasticbeanstalk.com/events
What just happened? You `GET` an info from the server!
Same thing happens once you open in a browser any Web page.
) Use for example a Chrome browser and go into the `Inspector` mode
) Open https://www.google.com
) See the first call in the `Network` tab. You `GET` pure HTML only
```
- Whole Web speaks `REST`. Once you understand its rules, you'll understand how everything works on the Web.
```
Why you can have an unofficial Twitter app on your mobile?
Why you can have 3rd party apps in Facebook
Why you can have a Google Map on your Web page
```

[ProgrammableWeb](http://www.programmableweb.com/) had 9000 APIs registered in 2013, this year (2016) they already have over 14,700 (April) and over 15,800 (September).

**Cool API**
- http://catfacts-api.appspot.com/doc.html
- http://catfacts-api.appspot.com/api/facts?number=3

## Consuming and Theory

- [API Clients](docu/apiclients.md)
- [API Reference](docu/apireference.md)

## Setting up a portal with REST API documentation 

- Do it with documentation listed in tutorial here https://github.com/YaaS/docpad-skeleton-apidocs#tutorial
- Do it with video support https://www.youtube.com/watch?v=a0i6kXxgYuwdoc
