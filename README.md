# Propeller Front End Coding Challenge (online)

## The latest and greatest mapping application in town!

At Propeller we love tiles - we love serving them and we love consuming them - much like :cake:. We need you to build a new front-end mapping application that can consume tiles from an online server and correctly grid / display them for the user.

We have a rough mockup from our designers and we need you to bring that vision to life.

## The Mockup

![This is only a guide to implementation and you can change this however you see fit](https://github.com/PropellerAero/frontend-coding-challenge/blob/main/prototype.png?raw=true)

## Background

Commonly large datasets like maps (2D or 3D) are broken down into chunks with varying levels of detail. You will already be familiar with this concept in e.g. Google Maps, where you can zoom out to see the whole world in low detail. Zoom in and you can see your house. [This blog post](https://macwright.org/2012/05/15/how-web-maps-work.html) provides a good overview.

## The Challenge

Create a simple React frontend app that displays the [tiles (available via our server)](https://github.com/PropellerAero/frontend-coding-challenge#where-can-i-get-my-tiles) in the style of a 2D map view. Please avoid using existing mapping frameworks such as Leaflet, Mapbox etc.

## Requirements

- Allow zooming using +/- buttons
- Allow scrolling when the content doesn't fit in the browser viewport.

## Extras

If you have time feel free to add any other extensions you think would demonstrate your ninja 🥷 coding skills and how you will be an awesome addition to the Propeller team.

Here are some possible ideas:

- allow panning of the tiles rather than scrolling
- if panning implemented switch to using scroll to zoom
- gradual zooming between tiles
- smooth transitions between tiles
- spice up you app with some styles

## Considerations

- Consider how your app is built.
- Consider coding style (e.g. robustness and maintainability).
- Block in some simple tests.

That is a long list of things, and we are aware of the fact that your time is limited. Therefore, please let us know some of the tradeoffs that you have made, what you have focussed on and what you have ignored for now.

## Implementation

It's ultimately up to you!

You can use online tools such as [codepen](https://codepen.io/) or [codesandbox](https://codesandbox.io/) (from a template React project) and send us the links.

If you want to go from scratch you can also create a react app (using Create React App) and send us the code / git repo. The app should be self contained and simple for us to build and run (e.g. provide npm install/build/start).

## Where can I get my tiles?

Tiles are available as a GET request at the url `https://challenge-tiler.services.propelleraero.com/:z/:x/:y?token=<id>` where z is the zoom level (0 being most zoomed out), x is the column, and y is the row. If the tile does not exist for a given zxy triplet the server will return a status code of `404`. Zoom only goes up to 3.

Your token will be sent to you as part of the challenge and this should be substituted in as the `token=<id>` query parameter. Missing or bad tokens will respond with a status code of `403`.

We have also included all the tiles available in the `/tiles` directory in this repository to give you an idea of what will be returned and the full image `un-tiled.jpg`.
