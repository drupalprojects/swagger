# Swagger API Module
---

This module provides a [Swagger/OpenAPI](https://github.com/OAI/OpenAPI-Specification) compliant document describing the enabled REST resources of your site.

## Setup
```
drush dl swagger
```

```
drush -y en swagger swagger_json_schema
```

## Documentation
Enable a REST endpoint ([REST UI](https://www.drupal.org/project/restui) is helpful here), and go one of these endpoints, depending on what kind of resource you enabled.

* /swagger/openapi/entities?_format=json (for entity resources like users or content)
* /swagger/openapi/non-entity?_format=json (for other types of resources)


The Open API specification document in JSON format that describes all of the
entity REST resources can be downloaded from, `swagger/openapi/entities?_format=json`.

[Learn more about the Open API specification](https://github.com/OAI/OpenAPI-Specification)

### Swagger UI module
To spin up a visual web UI for browsing REST API documentation, enable the Swagger UI module:

```
drush en -y swagger_ui
```

This module makes use of the [swagger-ui library](https://github.com/swagger-api/swagger-ui) in order to help provide a web interface for viewing REST API docs.
 
If you're using composer to manage the site (recommended) composer will install the Swagger UI library in /libraries/swagger-ui. Otherwise you can download it and move it here manually.
