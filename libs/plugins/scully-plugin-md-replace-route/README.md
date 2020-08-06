# scully-plugin-md-replace-route Plugin

## Description

This plugin replaces a route with an .md file.

## Type

Router Plugin

## Usage

In the application's scully.<your-app>.config.ts:

1. Configure the route that will render its content from a markdown file.

The route has an object containing a type `mdReplaceRoute` and the file's path.

```typescript
export const config: ScullyConfig = {
  routes: {
    '/': {
      type: 'mdReplaceRoute',
      file: './my-file.md',
    },
  },
};
```
