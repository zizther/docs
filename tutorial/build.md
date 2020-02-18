# 2. Build and Display Your Content

Now that we can work with Craft CMS locally, we’ll configure and edit our blog content and learn how to work with it on the front end.

We’ll start with our configuration and content editing in the control panel, then continue either with a Twig front end or Craft’s GraphQL API.

## Content in Craft CMS

TODO: overview of demo Sections, Entries, Field Layouts and Fields (include Globals?) **key point: flexibility**

## Choose your front end

TODO: compare working with Twig and GraphQL to someone who’s not done either, then link to template or GraphQL route

## Edit templates

Craft ships with the ability to create a dynamic front end using Twig templates.

TODO: explain markup, purpose of templates

TODO: mention other front end assets 

### Check out the example templates

### VS Code syntax highlighting

- Twig
- PHP
- JSON
- JavaScript?
- more useful plugins

## Fetch content with GraphQL

You can also use Craft CMS headlessly, meaning your web server provides an authoring experience but relies on outside code to provide the front end for visitors. In this case you won’t work with Twig templates, but Craft’s GraphQL API.

TODO: what is GraphQL

TODO: headless configuration

TODO: querying Entries, Globals, and Assets

TODO: sending data back to Craft (CSRF) ?