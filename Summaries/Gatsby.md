# Gatsby

### Folder structure (https://www.gatsbyjs.com/docs/reference/gatsby-project-structure/)

```
Copycopy code to clipboard
/
|-- /.cache
|-- /blog
|-- /plugins
|-- /public
|-- /src
    |-- /api
    |-- /pages
    |-- /templates
    |-- html.js
|-- /static
|-- gatsby-config.js
|-- gatsby-node.js
|-- gatsby-ssr.js
|-- gatsby-browser.js
```

### Folders

/.cache Automatically generated. This folder is an internal cache created automatically by Gatsby. The files inside this folder are not meant for modification. Should be added to the .gitignore file if not added already.

/plugins This folder hosts any project-specific (“local”) plugins that aren’t published as an npm package. Check out the plugin docs for more detail.

/public Automatically generated. The output of the build process will be exposed inside this folder. Should be added to the .gitignore file if not added already.

/src This directory will contain all of the code related to what you will see on the frontend of your site (what you see in the browser), like your site header, or a page template. “src” is a convention for “source code”.

/api JavaScript and TypeScript files under src/api become functions automatically with paths based on their file name. Check out the functions guide for more detail.
/pages Components under src/pages become pages automatically with paths based on their file name. Check out the pages recipes for more detail.
/templates Contains templates for programmatically creating pages. Check out the templates docs for more detail.
html.js For custom configuration of default .cache/default_html.js. Check out the custom HTML docs for more detail.
/static If you put a file into the static folder, it will not be processed by webpack. Instead it will be copied into the public folder untouched. Check out the assets docs for more detail.

### Files

You can also author all these files in TypeScript, see TypeScript and Gatsby for more details.

gatsby-browser.js: This file is where Gatsby expects to find any usage of the Gatsby browser APIs (if any). These allow customization/extension of default Gatsby settings affecting the browser.

gatsby-config.js: This is the main configuration file for a Gatsby site. This is where you can specify information about your site (metadata) like the site title and description, which Gatsby plugins you’d like to include, etc. Check out the config docs for more detail.

gatsby-node.js: This file is where Gatsby expects to find any usage of the Gatsby node APIs (if any). These allow customization/extension of default Gatsby settings affecting pieces of the site build process.

gatsby-ssr.js: This file is where Gatsby expects to find any usage of the Gatsby server-side rendering APIs (if any). These allow customization of default Gatsby settings affecting server-side rendering.

### Miscellaneous

The file/folder structure described above reflects Gatsby-specific files and folders. Since Gatsby sites are also React apps, it’s common to use standard React code organization patterns such as folders like /components and /utils inside /src. The React docs have more information on a typical React app folder structure.

### Gatsby

#### Using local fonts in Gatsby

Get started by using local fonts by adding them to your project. Copy the font file into your Gatsby project, for example, `src/fonts/fontname.woff2.`


You will need to create a new CSS rule to use your local font in your project. First, create a typography.css file and declare your @font-face selector.

```
/* roboto-regular - latin */
@font-face {
  font-family: 'Roboto';
  font-style: normal;
  font-weight: 400;
  src: url('../fonts/roboto-v30-latin-regular.eot'); /* IE9 Compat Modes */
  src: local(''),
       url('../fonts/roboto-v30-latin-regular.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
       url('../fonts/roboto-v30-latin-regular.woff2') format('woff2'), /* Super Modern Browsers */
       url('../fonts/roboto-v30-latin-regular.woff') format('woff'), /* Modern Browsers */
       url('../fonts/roboto-v30-latin-regular.ttf') format('truetype'), /* Safari, Android, iOS */
       url('../fonts/roboto-v30-latin-regular.svg#Roboto') format('svg'); /* Legacy iOS */
}

```