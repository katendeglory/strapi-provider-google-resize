# strapi-provider-upload-google-cloud-resize

This is just an extension of the amazing original project available here 👉

[strapi-provider-upload-google-cloud-storage](https://www.npmjs.com/package/strapi-provider-upload-google-cloud-storage)

It was made for a personal use, as the original project does not offer resizing capabilities.

## Installation

Install the package from your app root directory

with `npm`
```
npm install strapi-provider-upload-google-resize --save
```

or `yarn`
```
yarn add strapi-provider-upload-google-resize
```


**Example with one configuration for all environments (dev/stage/prod)**

`./extensions/upload/config/settings.json`
```json
{
  "provider": "google-cloud-resize",
  "providerOptions": {
    "serviceAccount": "<Your serviceAccount JSON object/string here>",
    "bucketName": "Bucket-name",
    "baseUrl": "https://storage.googleapis.com/{bucket-name}",
    "basePath": "",
    "publicFiles": true,
    "optimize": {
      "resize": true,
      "width": 1000,
		  "height": 1000,
			"quality": 75
    }
  }
}
```