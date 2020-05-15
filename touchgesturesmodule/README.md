# TouchGesturesModule

The `TouchGesturesModule` class enables touch gesture detection.

## Example

```text
//==============================================================================
// The following example demonstrates how to subscribe to all touch events to
// control the rotation, scale, position, material and opacity of a plane.
//
// Project setup:
// - Insert a plane
// - Increase the x and y-axis scale values of the plane to 2
// - Create two materials with different colors
// - Assign one of the materials to the plane
// - Enable all Touch Gestures under the Touch Gesture capability
//==============================================================================

// Load in the required modules
const Materials = require('Materials');
const Scene = require('Scene');
const TouchGestures = require('TouchGestures');

// Locate the plane in the Scene
const plane = Scene.root.find('plane0');

//==============================================================================
// Change the material applied to the plane when the plane is tapped
//==============================================================================

// Locate the materials in the Assets
const material = Materials.get('defaultMaterial0');
const material2 = Materials.get('defaultMaterial1');

// Subscribe to tap gestures on the plane
TouchGestures.onTap(plane).subscribe(function (gesture) {

  // Switch materials depending on which one is currently applied to the plane
  if(plane.materialIdentifier === material.identifier) {
    plane.material = material2;
  } else {
    plane.material = material;
  }

});

//==============================================================================
// Make the plane's material transparent when the plane is long pressed
//==============================================================================

// Subscribe to long press gestures on the plane
TouchGestures.onLongPress(plane).subscribe(function (gesture) {

  // Set the opacity to 50%
  plane.material.opacity = 0.5;

  // Subscribe to the state of the gesture
  gesture.state.monitor().subscribe(function (state) {

    // Return the opacity to 100% when the gesture ends
    if(state.newValue !== 'BEGAN' && state.newValue !== 'CHANGED') {
      plane.material.opacity = 1;
    }

  });

});

//==============================================================================
// Move the plane across the screen when dragging it with a finger
//==============================================================================

// Store a reference to the transform of the plane
const planeTransform = plane.transform;

// Subscribe to pan gestures on the plane
TouchGestures.onPan(plane).subscribe(function (gesture) {

  // Translate the position of the finger on the screen to the plane's
  // co-ordinate system
  const gestureTransform = Scene.unprojectToFocalPlane(gesture.location);

  // Update the position of the plane
  planeTransform.x = gestureTransform.x;
  planeTransform.y = gestureTransform.y;

});

//==============================================================================
// Scale the plane when pinching it with two fingers
//==============================================================================

// Subscribe to pinch gestures on the plane
TouchGestures.onPinch(plane).subscribe(function (gesture) {

  // Store the last known x and y-axis scale values of the plane
  const lastScaleX = planeTransform.scale.x.pinLastValue();
  const lastScaleY = planeTransform.scale.y.pinLastValue();

  // Update the scale of the plane by multiplying the last known scale with the
  // scale returned by the gesture
  planeTransform.scaleX = gesture.scale.mul(lastScaleX);
  planeTransform.scaleY = gesture.scale.mul(lastScaleY);

});

//==============================================================================
// Rotate the plane when rotating it with two fingers
//==============================================================================

// Subscribe to rotation gestures on the plane
TouchGestures.onRotate(plane).subscribe(function (gesture) {

  // Store the last known z-axis rotation value of the plane
  const lastRotationZ = planeTransform.rotationZ.pinLastValue();

  // Update the z-axis rotation of the plane by adding the gesture rotation and
  // multiply it by -1 to have it rotate in the correct direction
  planeTransform.rotationZ = gesture.rotation.mul(-1).add(lastRotationZ);

});
```

## Properties

This module exposes no properties.

## Methods

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>onLongPress</code>
      </td>
      <td style="text-align:left">
        <p><code>onLongPress(): EventSource onLongPress(object: SceneObjectBase): EventSource onLongPress(options: {object?: SceneObjectBase, normalizeCoordinates?: boolean}): EventSource</code>
        </p>
        <p>Returns an <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/eventsource_class"><code>EventSource</code></a>,
          to which you may subscribe, that emits a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/touchgestures_module/longpressgesture_class"><code>LongPressGesture</code></a> object
          for each long-press interaction.</p>
        <p>When <code>object</code> is specified, only events for the specified object
          are emitted.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>onPan</code>
      </td>
      <td style="text-align:left">
        <p><code>onPan(): EventSource onPan(object: SceneObjectBase): EventSource onPan(options: {object?: SceneObjectBase, normalizeCoordinates?: boolean}): EventSource</code>
        </p>
        <p>Returns an <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/eventsource_class"><code>EventSource</code></a>,
          to which you may subscribe, that emits a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/touchgestures_module/pangesture_class"><code>PanGesture</code></a> object
          for each pan interaction.</p>
        <p>When <code>object</code> is specified, only events for the specified object
          are emitted.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>onPinch</code>
      </td>
      <td style="text-align:left">
        <p><code>onPinch(): EventSource onPinch(object: SceneObjectBase): EventSource onPinch(options: {object?: SceneObjectBase, normalizeCoordinates?: boolean}): EventSource</code>
        </p>
        <p>Returns an <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/eventsource_class"><code>EventSource</code></a>,
          to which you may subscribe, that emits a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/touchgestures_module/pinchgesture_class"><code>PinchGesture</code></a> object
          for each pinch interaction.</p>
        <p>When <code>object</code> is specified, only events for the specified object
          are emitted.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>onRotate</code>
      </td>
      <td style="text-align:left">
        <p><code>onRotate(): EventSource onRotate(object: SceneObjectBase): EventSource onRotate(options: {object?: SceneObjectBase, normalizeCoordinates?: boolean}): EventSource</code>
        </p>
        <p>Returns an <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/eventsource_class"><code>EventSource</code></a>,
          to which you may subscribe, that emits a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/touchgestures_module/rotategesture_class"><code>RotateGesture</code></a> object
          for each rotate interaction.</p>
        <p>When <code>object</code> is specified, only events for the specified object
          are emitted.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>onTap</code>
      </td>
      <td style="text-align:left">
        <p><code>onTap(): EventSource onTap(object: SceneObjectBase): EventSource onTap(options: {object?: SceneObjectBase, normalizeCoordinates?: boolean}): EventSource</code>
        </p>
        <p>Returns an <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/eventsource_class"><code>EventSource</code></a>,
          to which you may subscribe, that emits a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/touchgestures_module/tapgesture_class"><code>TapGesture</code></a> object
          for each tap interaction.</p>
        <p>When <code>object</code> is specified, only events for the specified object
          are emitted.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`Gesture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/touchgesturesmodule.gesture) | The `Gesture` class encapsulates details of a detected gesture. |
| [`LongPressGesture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/touchgesturesmodule.longpressgesture) | The `LongPressGesture` class contains the details of a detected long-press gesture. |
| [`PanGesture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/touchgesturesmodule.pangesture) | The `PanGesture` class contains the details of a detected pan gesture. |
| [`PinchGesture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/touchgesturesmodule.pinchgesture) | The `PinchGesture` class contains the details of a detected pinch gesture. |
| [`RawTouchGesture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/touchgesturesmodule.rawtouchgesture) | The RawTouchGesture class encapsulates raw touch data. |
| [`RotateGesture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/touchgesturesmodule.rotategesture) | The `RotateGesture` class contains the details of a detected rotate gesture. |
| [`TapGesture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/touchgesturesmodule.tapgesture) | The `TapGesture` class contains the details of a detected tap gesture. |

