# HandTrackingModule

The `HandTrackingModule` class enables hand tracking.

## Example

```text
//==============================================================================
// The following example demonstrates how to bind the position of a plane to a
// hand.
//
// Project setup:
// - Insert a plane
//==============================================================================

// Load in the required modules
const HandTracking = require('HandTracking');
const Scene = require('Scene');

// Locate the plane and focal distance in the Scene
const plane = Scene.root.find('plane0');
const focalDistance = Scene.root.find('Focal Distance');

// Store a reference to a detected hand
const hand = HandTracking.hand(0);

// Store the z-axis position signal of the focal distance
const focalDistanceZPosition = focalDistance.transform.z;

// Bind the cameraTransform of the hand to the plane's transform
plane.transform = hand.cameraTransform;

// Additionally overwrite the z-axis values with distance taken into account
plane.transform.z = hand.cameraTransform.z.sub(focalDistanceZPosition);

// Bind the hidden property of the plane to a boolean signal that returns true
// when no hands have been detected
plane.hidden = HandTracking.count.eq(0);
```

## Properties

<table>
  <thead>
    <tr>
      <th style="text-align:left">Property</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>count</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) count: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> indicating the number of detected
          hands.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>hand</code>
      </td>
      <td style="text-align:left">
        <p><code>hand(index: Number): Hand</code>
        </p>
        <p>Returns the <code>Hand</code> indicated by index.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`Hand`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/handtrackingmodule.hand) | The `Hand` class describes a hand detected in a scene. |

