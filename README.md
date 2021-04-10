# gridsome-source-directus9

Based on https://github.com/peXed/gridsome-source-directus, updated to support Directus 9

### Basic usage:

Since this package is not (yet) published on npm, just clone the repo and add it to your package.json file:
```javascript 
{
  "dependencies": {
    "gridsome-source-directus9": "path/to/cloned/project/folder",
  },
}
```

Add this in your gridsome.config.js:
```javascript 
module.exports = {
  plugins: [
    {
      use: "gridsome-source-directus9",
      options: {
        apiUrl: "",
        project: "Directus", //name of project in directus
        email: "", //email for login to directus
        password: "", //password for login to directus
        collections: [ //example collections, read more about the options here: https://github.com/peXed/gridsome-source-directus
          {
            name: "articles",
            status: "published",
            fields: "*.*",
            downloadImages: true,
            hasRoute: true
          },
          {
            name: "projects",
            status: "published",
            fields: "*.*",
            downloadImages: true,
          },
          {
            name: "pages",
            status: "published",
            fields: "*.*.*",
            downloadImages: true,
            hasRoute: true
          }
        ],
      },
    },
  ],
  ```
