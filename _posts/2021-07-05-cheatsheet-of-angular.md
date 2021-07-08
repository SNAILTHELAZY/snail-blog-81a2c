---
title: Cheatsheet of Angular
date: '2021-07-05'
thumb_img_alt: lorem-ipsum
content_img_alt: lorem-ipsum
seo:
  title: ''
  description: ''
  robots: []
  extra: []
  type: stackbit_page_meta
layout: post
excerpt: You can find useful tricks and commands in here
---
## CLI Command

### 1.Creating Project:

`ng new [project-name]`

### 2.Serve the project locally:

`ng serve`

This will create the server locally. If you wish to open a new window upon the completion of compiling, add the o flag after the command and the above command will become this:

`ng serve -o`

### 3.Create a new elements:

`ng generate [element] [element-name]`

For element, you can substitute it into the following:

*   Components. It works as the same way as components in React. It defines how should this component display, logics for handling events occurred within the component, etc.

*   Services. Functions does not affect the UI directly will goes there. I usually create HttpService of myself to handle request that send to the server

*   Directives. It adds behaviour in the components template. You can change the templates styles or control components behaviour. For example, NgFor, NgIf are directives help structuring the templates.

*   Pipes

*   Classes. This is the Model of Angular's MVC approach. It defines the logics of a data entity.

### 4.Running Unit Test:

`ng test`

This will run the unit test written in the .spec.ts. Which the is the components of your project.

### 5.Build the project and export it:

`ng build`

This will compile the project into a bundle of HTML, CSS and JS in the dist directory.

## Proxying
There are 2 ways to proxy your server, in case your server and the app is not at the same origin.

But first, you will need to prepare a proxy configuration file, it can be either js file or json, depending on how many paths you have to proxy to your server:

1. proxying only one path
```json
{
  "/api": {
    "target": "http://localhost:3000",
    "secure": false
  }
}
```

2. proxying multiple paths
```js
const PROXY_CONFIG = [
    {
        context: //paths you need to proxy, it should be an array
        ,
        target: "http://localhost:3000",
        secure: false
    }
]

module.exports = PROXY_CONFIG;
```

Then, you can either

## Syntaxes of Structural Directives
