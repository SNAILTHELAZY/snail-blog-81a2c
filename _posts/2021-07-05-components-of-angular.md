---
title: Components of Angular
date: '2021-07-05'
thumb_img_alt: lorem-ipsum
content_img_alt: lorem-ipsum
excerpt: lorem-ipsum
seo:
  title: ''
  description: ''
  robots: []
  extra: []
  type: stackbit_page_meta
layout: post
---
Components is the main elements in Angular, which the application is consists of at least one component. It can be created through the following command:

ng generate component \[component-name]

A component always consists of the following:

1.  HTML indicates how the component show.

2.  CSS for styling the component

3.  TypeScript(TS) for handling events and interaction occurred, also the logics within the component.

## Component Lifecycle

Every components has its own lifecycle. And the most common-used lifecycle method is OnInit(), which is called upon the initialization of the component.

As the timing of the lifecycles hooks are quite complicated, it requires a diagram to explain:

Image

As you can see, there are many hooks just called once, while some of them will be called constantly when the dataOnChanges is fired.

The DataOnChanges is fired whenever the inputs are changed.

## Interactions between Components

Before we go through components work with each other. We should know the meaning of the following brackets:

*   \[]. It binds data to elements' property.

*   (). It binds methods to elements' event.

In Angular, relationship between components works like a family tree, which there will be an ancestor called root, also known as app-comppnent in every Angular project. Then the app-component has many descendants, the descendants are siblings to each other. Some of the descendants have its own child, and some don't.

When there are many components, let's say a top-app-bar component is created for the user to search products, while there is a component called product-list for displaying the products that meets the search criteria. And their relationship is look like this:

Image

In order to show the products, it is required to transfer data from the top-app-bar to the product-list. So the @Input() is introduced to help transferring data fetched in the top-app-bar to the product-list. The programming example excerpt will be like this:
