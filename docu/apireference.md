# API Reference

Let us talk about the REST API specification (yawn)

HTTP/1.1 Specification: https://tools.ietf.org/html/rfc2616

## Theory

### Base URI and Paths/Endpoints/Resources

Base URI: `http://minerva.us-west-2.elasticbeanstalk.com`

and

Paths/Endpoints/Resources: `/events` or `/events/{eventId}`

### Methods

Most commonly used:
- GET
- POST
- PUT
- DELETE

Make a GET call to `http://minerva.us-west-2.elasticbeanstalk.com/events`

### Query params

So called optional parameters.
Its about limiting and specifying response.

Make a GET call to `http://minerva.us-west-2.elasticbeanstalk.com/events?q=type:"Conference 2016"`

### Headers

Response and request.

Make again a GET call to `http://minerva.us-west-2.elasticbeanstalk.com/events`
Notice all the different headers, content type or length.

### Body/Payload

It is not only when you POST but also whey you get a response.

Make a POST call with Content-Type: application/json
```
{  
   "type":"sample type",
   "name":"sample name",
   "description":"sample description",
   "website":"sample website",
   "start_date":"sample start_date",
   "end_date":"sample end_date",
   "address":"sample address",
   "latitude":1.1,
   "longitude":1.1,
   "eventId":"sampleeventId"
}
```

Check also the response body.

### Schemas and Mixins

**It is all about the body**

Schema says what are the main service readable attributes: http://jsonschema.net/
Mixins say that you can basically put whatever you want.

- Useful for validation
- Gives a good overview of what data have to be provided

Make a POST call with Content-Type: application/json
```
{  
   "type":"sample type",
   "name":"sample name"
}
```

### Response body and codes

All listed here: https://httpstatuses.com/

- 200
- 400
- 500

Make again a GET call to `http://minerva.us-west-2.elasticbeanstalk.com/events`
Make again a POST call with Content-Type: application/json
```
{  
   "type":"sample type",
   "name":"sample name",
   "description":"sample description",
   "website":"sample website",
   "start_date":"sample start_date",
   "end_date":"sample end_date",
   "address":"sample address",
   "latitude":1.1,
   "longitude":1.1,
   "eventId":"sampleeventId"
}
```

The same call twice.

## Document using RAML or API Blueprint

RAML spec: https://github.com/raml-org/raml-spec/blob/master/versions/raml-08/raml-08.md
Go to https://github.com/derberg/minerva/blob/master/service/api/api.raml

Develop with approach **API First** then you get:
- API Reference: http://derberg.github.io/services/minerva/latest/index.html#ApiReference
- API Console: http://derberg.github.io/services/minerva/latest/apiconsole.html
- API Notebook: http://derberg.github.io/services/minerva/latest/index.html#Gettingconferenceeventsfor2016
- API Client: http://derberg.github.io/services/minerva/latest/client.zip

Write it using:
- API Designer: https://github.com/mulesoft/api-designer
- Restlet Studio: https://studio.restlet.com/
