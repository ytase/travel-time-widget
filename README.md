# Yta.se travel time widget specifications - v1.0.0-Alpha.2

Yta.se travel time widget allows you to include a map showing the travel time from a point of origin with different transportation modes (walking, by car, using public transports).

Please note that the specifications are currently in alpha and might be subject to change.

## Requirements

To use the yta.se travel time widget, you will have to include in the page:
- an iframe pointing towards the yta.se travel time widget
- the following text underneath the iframe: `Restider presenteras tillsammans med yta.se.`. In the text, `yta.se` should link to `https://yta.se`. Note that you are allowed to include a descriptive text between the widget and that text if you want to.

## Usage

### Iframe source

The iframe source is `//external.yta.se/widgets/travel-time?WIDGET_PARAMETERS`

The parameters supported are:

- __origin (required)__: `lat,lng` The latitudes and longitudes of the point of origin. The travel times will be computed from the coordinates specified here. Both latitudes and longitude must be WSG 84 coordinates. 
    ex: `origin=59.338900,18.060416`

### Iframe parameters

__allowfullscreen__: required to let the suer the possibility to have a full screen view of the map
__frameborder="0"__: needed to remove borders around the iframe in some browser.

### Example of basic usage

```js
<iframe height="320" width="520" src="//external.yta.se/widgets/travel-time?origin=59.338900,18.060416" frameborder="0" allowfullscreen>
</iframe>
<div>Restider presenteras tillsammans med <a href="https://yta.se">yta.se</a>.</div>
```
