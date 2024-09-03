# OpenAPI
Reference: [link](https://fastapi.tiangolo.com/tutorial/first-steps/#what-is-openapi-for)

FastAPI creates a "schema" for your entire API using the OpenAPI standard.

| **Concept** | **Explanation** |
| ---- | ---- |
| Schema Definition | - A "schema" is an abstract description or definition of something, not the actual implementation. |
| API Schema | - OpenAPI is a specification that defines the schema of your API.<br>- This schema includes API paths, possible parameters, and more. |
| Data Schema | Refers to the shape or structure of data, such as the attributes and data types in a JSON object. |
| OpenAPI and JSON Schema | - OpenAPI defines the overall API schema.<br>- Uses JSON Schema to describe the data sent and received by your API. |
| openapi.json | - FastAPI automatically generates a JSON schema (openapi.json) that includes descriptions of all your API paths.<br>- This file provides a raw view of the OpenAPI schema. |
`openapi.json` can be found at: http://127.0.0.1:8000/openapi.json
```json
{
    "openapi": "3.1.0",
    "info": {
        "title": "FastAPI",
        "version": "0.1.0"
    },
    "paths": {
        "/items/": {
            "get": {
                "responses": {
                    "200": {
                        "description": "Successful Response",
                        "content": {
                            "application/json": {



...
```

**What is OpenAPI for?**

- The OpenAPI schema powers the interactive documentation systems provided by FastAPI.
- Many alternatives based on OpenAPI are available and can be added to FastAPI applications.
- The OpenAPI schema can be used to automatically generate code for clients that interact with your API, including frontend, mobile, or IoT applications.

**Operation**

"Operation" here refers to one of the HTTP "methods". One of:
- POST: to create data
- GET: to read data
- PUT: to update data
- DELETE: to delete data

and the more exotic ones:
- OPTIONS
- HEAD
- PATCH
- TRACE
In the HTTP protocol, you can communicate to each path using one (or more) of these "methods".

