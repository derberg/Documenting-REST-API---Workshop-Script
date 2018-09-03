# API Reference

Let us talk about the REST API specification (yawn)

HTTP/1.1 Specification: https://tools.ietf.org/html/rfc2616

## Theory

### Base URI and Paths/Endpoints/Resources

Base URI: `https://api.thecatapi.com/v1`

and

Paths/Endpoints/Resources: `/images` or `/images/:image_id`

### Methods

Most commonly used:
- GET
- POST
- PUT
- DELETE

Make a GET call to `https://api.thecatapi.com/v1/images/search`

### Query params

So called optional parameters.
Its about limiting and specifying response.

Make a GET call to `https://api.thecatapi.com/v1/images/search?size=small&limit=5`

### Headers

Response and request.

Make again a GET call to `https://api.thecatapi.com/v1/images/search`
Notice all the different headers, content type or length.

### Body/Payload

It is not only when you POST but also whey you GET a response.

Make a POST call to `https://api.thecatapi.com/v1/favourites` with `Content-Type: application/json`
```
{
	"image_id": "4m6"
}
```

Check also the response body.
Then DELETE what you just created.

### Schemas and Mixins

**It is all about the body**

Schema says what are the main service readable attributes: http://jsonschema.net/
Mixins say that you can basically put whatever you want.

- Useful for validation
- Gives a good overview of what data have to be provided

Make a POST call with Content-Type: application/json
```
{
	"image_ids": "4m6"
}
```

Notice the validation error message in response.

### Response body and codes

All listed here: https://httpstatuses.com/

- 200
- 400
- 500

Make again a GET call to `https://api.thecatapi.com/v1/favourites`
Make again a POST call with Content-Type: application/json
```
{
	"image_id": "4m6"
}
```

## Document using Swagger aka OpenAPI Spec

Swagger spec: https://github.com/OAI/OpenAPI-Specification
Sample spec in use: https://editor.swagger.io/

## Document using RAML

RAML spec: https://github.com/raml-org/raml-spec/blob/master/versions/raml-08/raml-08.md
Go to https://github.com/derberg/minerva/blob/master/service/api/api.raml

Develop with approach **API First** then you get:
- API Reference: http://derberg.github.io/services/minerva/latest/index.html#ApiReference (using https://github.com/raml2html/raml2html behind the scenes)
- API Console: http://derberg.github.io/services/minerva/latest/apiconsole.html (using https://github.com/mulesoft/api-console behind the scenes)
- API Notebook: http://derberg.github.io/services/minerva/latest/index.html#Gettingconferenceeventsfor2016 (using https://github.com/mulesoft/api-notebook behind the scenes)
- API Client: http://derberg.github.io/services/minerva/latest/client.zip (using https://github.com/mulesoft-labs/raml-javascript-generator behind the scenes)

Write it using:
- API Designer: https://github.com/mulesoft/api-designer
- Restlet Studio: https://studio.restlet.com/

Alternatives:
- API Blueprint
- Apiary
- Swagger
