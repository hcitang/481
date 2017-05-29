
# Line Drawing: Mouse Handling

This tutorial walks you through making a Canvas on which you can do some line drawing, so you can drag your mouse around the canvas, and this will draw some lines -- kind of like a painting program. The way this works is that `MouseDown` (fired when someone presses a mouse button), `MouseUp` (fired when someone releases a mouse button) and `MouseMove` (fired when someone moves a mouse over the UI element, regardless of whether a mouse button is pressed or not)events are captured, and responded to accordingly. In particular, when the `MouseMove` event is fired, if the mouse button is pressed, then it adds a new `Line` to the canvas between the current mouse point, and the previous mouse point.

[](https://www.youtube.com/watch?v=VNPmXhII754)

[source video](https://www.youtube.com/watch?v=VNPmXhII754)

**Knowledge:** Mouse event handlers can be assigned to most UI elements. For instance, they can be assigned to `Buttons`, `Labels` and so on. Of course, setting these up can override default behaviour.
