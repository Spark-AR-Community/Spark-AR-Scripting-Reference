# FaceTrackingModule

The `FaceTrackingModule` class enables tracking faces in 3D.

## Example

```text
//==============================================================================
// The following example demonstrates how to control the rotation and scale of
// an object using face rotation and mouth openness.
//
// Project setup:
// - Insert a plane
//==============================================================================

// Load in the required modules
const FaceTracking = require('FaceTracking');
const Scene = require('Scene');

// Locate the plane in the Scene
const plane = Scene.root.find('plane0');

// Store a reference to a detected face
const face = FaceTracking.face(0);

//==============================================================================
// Control the rotation of the plane with the rotation of the face
//==============================================================================

// Store references to the transform of the plane and face
const planeTransform = plane.transform;
const faceTransform = face.cameraTransform;

// Bind the rotation of the face to the rotation of the plane
planeTransform.rotationX = faceTransform.rotationX;
planeTransform.rotationY = faceTransform.rotationY;
planeTransform.rotationZ = faceTransform.rotationZ;

//==============================================================================
// Control the scale of the plane with mouth openness
//==============================================================================

// Store a reference to the mouth openness with some additional mathematical
// operations to amplify the signal
const mouthOpenness = face.mouth.openness.mul(4).add(1);

// Bind the mouthOpenness signal to the x and y-axis scale signal of the plane
planeTransform.scaleX = mouthOpenness;
planeTransform.scaleY = mouthOpenness;
```

## Properties

|Property|Description|
|:---|:---|
|`count`|`(get) count: ScalarSignal (set) (Not Available)` <br /> Returns a `ScalarSignal` representing the number of faces tracked in the scene.|

## Methods

|Method|Description|
|:---|:---|
| `face` | `face(index: number): Face` <br /> Returns the `Face` object from the detected face array at the specified index.|

## Classes

| Class | Description |
| :--- | :--- |
| [`Cheek`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetrackingmodule.cheek) | The `Cheek` class exposes the details of a detected cheek. |
| [`Chin`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetrackingmodule.chin) | The `Chin` class exposes the details of a detected chin. |
| [`Eye`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetrackingmodule.eye) | The `Eye` class exposes the details of a detected eye. |
| [`Eyebrow`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetrackingmodule.eyebrow) | The `Eyebrow` class exposes the details of a detected eyebrow. |
| [`Face`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetrackingmodule.face) | The `Face` class exposes details of a tracked face. |
| [`Forehead`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetrackingmodule.forehead) | The `Forehead` class exposes the details of a detected forehead. |
| [`Mouth`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetrackingmodule.mouth) | The `Mouth` class exposes the details of a detected mouth. |
| [`Nose`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetrackingmodule.nose) | The `Nose` class exposes the details of a detected nose. |

