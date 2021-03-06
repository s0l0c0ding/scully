---
title: plugins
published: true
lang: en
navlist_position: 1
navlist_parentIndex: true
---

# Plugins <!-- omit in toc -->

## Overview <!-- omit in toc -->

Scully uses a plugin system which allows users to define new ways for Scully to pre-render an application.  
It is simple to [register a new plugin](/docs/learn/plugins/register-a-new-plugin).

## Types <!-- omit in toc -->

There are six main types of plugins which allow code to be injected into various stages of the Scully process lifecycle:

<div class="docs-toc no-spacing"></div>

- [`allDone`](#alldone)
- [`fileHandler`](#filehandler)
- [`render`](#render)
- [`route process`](#routeprocess)
- [`routeDiscoveryDone`](#routediscoverydone)
- [`router`](#router)

#### [`router`](/docs/learn/plugins/types/router)

`router` plugins teach Scully how to get the required data to be pre-render pages from the route-params.

#### [`render`](/docs/learn/plugins/types/render)

`render` plugins are used to transform the rendered HTML.  
After the Angular application renders, the HTML content is passed to a `render` plugin where it can be further modified.

#### [`fileHandler`](/docs/learn/plugins/types/file-handler)

`fileHandler` plugins are used by the [`contentFolder`](/docs/learn/plugins/built-in-plugins/contentFolder) plugin during the render process. The [`contentFolder`](/docs/learn/plugins/built-in-plugins/contentFolder) plugin processes the folders for markdown files or other file type the folders may contain. The render process processes any existing `fileHandler` plugin for any file extension type.

#### [`routeDiscoveryDone`](/docs/learn/plugins/types/routeDiscoveryDone)

`routeDiscoveryDone` plugins are called automatically after all routes have been collected and all router plugins have finished.

#### [`allDone`](/docs/learn/plugins/types/allDone)

`allDone` plugins are like `routeDiscoveryDone` plugins, except they are called _after_ Scully finishes executing all its processes.

<div class="docs-prev_next">
  <a class="next" href="/docs/learn/plugins/register-a-new-plugin">register a new plugin</a>
</div>
