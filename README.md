# Getting Started

The full Swagger API can be found at the [Ignyte Platform Swagger](https://integration.ignyteplatform.com/swagger/index.html).

After obtaining the API key from your Ignyte Instance Settings Area, click "Authorize" in the Swagger link above, then enter the ``Bearer <api key>``. 

Next, use cURL to call the data. An example request URL is ``https://integration.ignyteplatform.com/api/v1/asset/<path>`` where path can be asset type, impacts, locations, departments, fields, custom drop down, etc. Please note: some paths require additional path information. For example:

``curl -X 'GET' \
  'https://integration.ignyteplatform.com/api/v1/asset/departments/westfield' \
  -H 'accept: text/plain'``
  
The location 'westfield' must be defined before requesting department data. 

Finally, assets can be deleted by asset ID and only asset types may be defined using the post method.

# Directory Structure

## The `OpenAssetsAPI` folder

This folder contains the Ignyte Platform's Asset API entrypoint within `openapi.yaml`.

## The `components` folder

This defines the scheme(s) the Ignyte Platform Asset API uses for security (e.g., OAuth2, API Key, etc.) as well as the object schemas.

## The `paths` folder

This defines each endpoint of the Ignyte Platform Assets API. A path can have one operation per http method.

## Support

For support using this API contact support@ignyteplatform.com. For inquiries about Ignyte Assurance Platform, contact info@ignyteplatform.com.
