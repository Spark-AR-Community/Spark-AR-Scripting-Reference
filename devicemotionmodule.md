# DeviceMotionModule

The `DeviceMotionModule` class enables device movement detection.

## Example

```text
//==============================================================================
// The following example demonstrates how to bind device rotation to an object.
//
// Project setup:
// - Insert a plane
// - Make sure the Device Motion capability is added in the properties
//==============================================================================

// Load in the required modules
const DeviceMotion = require('DeviceMotion');
const Scene = require('Scene');

// Locate the plane in the Scene
const plane = Scene.root.find('plane0');

// Store a reference to the transform of the plane and the world transform of
// the DeviceMotion module
const planeTransform = plane.transform;
const deviceWorldTransform = DeviceMotion.worldTransform;

// Bind the rotation of the device to the plane
planeTransform.rotationX = deviceWorldTransform.rotationX;
planeTransform.rotationY = deviceWorldTransform.rotationY;
planeTransform.rotationZ = deviceWorldTransform.rotationZ;
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
      <td style="text-align:left"><code>worldTransform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) worldTransform: TransformSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>TransformSignal</code> representing the device transformation
          relative to world coordinate system.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Classes

This module exposes no classes.

