# Media urls Contentful ui extension

## media-url-contentful-ui-extension

A PoC UI Extension for Contentful that pulls URLs out of Asset or Asset Array fields that are siblings of this field to make it easier to copy them out.

Displays a small thumbnail of the image also.

## Installation/usage

Install deps through `npm install`

```
export CONTENTFUL_MANAGEMENT_ACCESS_TOKEN=<your token>
```

Create:

```
contentful-extension create --space-id <your space id>
```

Works on Symbol (short text) fields only. Doesn't store a value, it is only used as a vanity/display helper.

It will look for any sibling fields that are Asset or Arrays of Assets and display the URLs for those. It automatically updates if the Entry is changed (image added/removed for example).

## Known issues/constraints
- Doesn't pull draft asset urls
- Displays broken image thumbnail for non-image assets
