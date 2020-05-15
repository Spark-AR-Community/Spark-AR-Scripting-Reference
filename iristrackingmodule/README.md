# IrisTrackingModule

The `IrisTrackingModule` class allows you to track the location of people's irises in your effect, to create effects such as eye color replacement.

## Example

```text
//==============================================================================
// The following example demonstrates how to bind the position and rotation of
// objects to the eyeball and iris.
//
// Project setup:
// - Insert two planes
// - (Recommended) Decrease the scale of the planes and assign materials to them
//==============================================================================

// Load in the required modules
const FaceTracking = require('FaceTracking');
const IrisTracking = require('IrisTracking');
const Scene = require('Scene');

// Locate the planes in the Scene
const centerPlane = Scene.root.find('plane0');
const irisPlane = Scene.root.find('plane1');

// Store a reference to a detected face
const face = FaceTracking.face(0);

// Store a reference to the left eyeball
const leftEyeball = IrisTracking.leftEyeball(face);

// Store a reference to the center and iris plane's transform
const centerPlaneTransform = centerPlane.transform;
const irisPlaneTransform = irisPlane.transform;

// Store references to the eyeball center, iris and rotation
const leftEyeballCenter = leftEyeball.center;
const leftEyeballIris = leftEyeball.iris;
const leftEyeballRotation = leftEyeball.rotation.eulerAngles;

// Bind the position of the eyeball center to the center plane
centerPlaneTransform.x = leftEyeballCenter.x;
centerPlaneTransform.y = leftEyeballCenter.y;
centerPlaneTransform.z = leftEyeballCenter.z;

// Bind the position of the the eyeball iris to the iris plane
irisPlaneTransform.x = leftEyeballIris.x;
irisPlaneTransform.y = leftEyeballIris.y;
irisPlaneTransform.z = leftEyeballIris.z;

// Bind the rotation of both planes to the eyeball rotation
centerPlaneTransform.rotationX = leftEyeballRotation.x;
centerPlaneTransform.rotationY = leftEyeballRotation.y;
centerPlaneTransform.rotationZ = leftEyeballRotation.z;

irisPlaneTransform.rotationX = leftEyeballRotation.x;
irisPlaneTransform.rotationY = leftEyeballRotation.y;
irisPlaneTransform.rotationZ = leftEyeballRotation.z;
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
      <td style="text-align:left"><code>leftEyeball</code>
      </td>
      <td style="text-align:left">
        <p><code>leftEyeball(face: Face): Eyeball</code>
        </p>
        <p>Returns an <code>Eyeball</code> object for the given face, containing information
          about the 3D position of the left eyeball.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rightEyeball</code>
      </td>
      <td style="text-align:left">
        <p><code>rightEyeball(face: Face): Eyeball</code>
        </p>
        <p>Returns an <code>Eyeball</code> object for the given face, containing information
          about the 3D position of the right eyeball.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`Eyeball`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/iristrackingmodule.eyeball) | The `Eyeball` class exposes details of a tracked eyeball. |

