
Leaflet.TouchHover
==================

A plugin for adding hover-like interaction to Leaflet maps on mobile devices. Created by [Vladimir Agafonkin](https://github.com/mourner).

## What it does

One problem with implementing hover interaction on mobile devices is that there are no `mouseover` and `mouseout` equivalents on mobile
(the spec has `touchenter` and `touchleave` events but they don't work in iOS).

Another problem is that touch-and-move interaction for hovering on features conflicts with the standard dragging functionality in interactive maps.

This plugin solves both problems by introducing **a button control that switches the map to "hover" mode**,
in which dragging and pinch zoom are disabled, and all the mouse hover events actually work when you touch and move over features as they would on a desktop browser.

If you have a Leaflet app that's designed to work with `mouseover`, `mouseout` and `mousemove` events on desktop browser, it will become usable on mobile with this plugin out of the box.

## Requirements

[Leaflet](http://leafletjs.com) 0.6.2 and later.

## Usage

```js
if (L.Browser.touch) {
	L.control.touchHover().addTo(map);
}
```

## License

Licensed under [The MIT License](http://opensource.org/licenses/MIT).
