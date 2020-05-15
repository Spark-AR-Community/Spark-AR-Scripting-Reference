# FaceTracking2DModule

The `FaceTracking2DModule` class enables tracking faces in 2D.

## Example

```text
//==============================================================================
// The following example demonstrates how to bind the position of a rectangle to
// a 2D face.
//
// Project setup:
// - Insert a rectangle
//==============================================================================

// Load in the required modules
const FaceTracking2D = require('FaceTracking2D');
const Scene = require('Scene');

// Locate the rectangle in the Scene and store its transform
const rectangle = Scene.root.find("rectangle0");
const rectangleTransform = rectangle.transform;

// Locate the canvas in the Scene and store the width and height
const canvas = Scene.root.find("canvas0");
const canvasBounds = canvas.bounds;
const canvasBoundsWidth = canvasBounds.width;
const canvasBoundsHeight = canvasBounds.height;

// Store the bounding box center of a detected face
const face2D = FaceTracking2D.face(0);
const face2DBounds = face2D.boundingBox;
const face2DBoundsCenter = face2DBounds.center;

// Convert the normalized screen space value for x and y by multiplying by the
// width and height of the canvas
const scaledX = face2DBoundsCenter.x.mul(canvasBoundsWidth);
const scaledY = face2DBoundsCenter.y.mul(canvasBoundsHeight);

// Subtract the half the width/height to center the plane correctly and multiply
// the y-position by -1, this is necessary because 0,0 in the canvas is the
// bottom left of the device
const rectangleX  = scaledX.sub(canvasBoundsWidth.div(2));
const rectangleY = scaledY.sub(canvasBoundsHeight.div(2)).mul(-1);

// Bind the new values to the x and y-axis positions of the rectangle
rectangleTransform.x = rectangleX;
rectangleTransform.y = rectangleY;
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
        <p>Returns a <code>ScalarSignal</code> representing the number of faces tracked
          in the scene.</p>
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
      <td style="text-align:left"><code>face</code>
      </td>
      <td style="text-align:left">
        <p><code>face(index: number): Face2D</code>
        </p>
        <p>Returns the <code>Face2D</code> object from the detected face array at the
          specified index.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`Face2D`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/facetracking2dmodule.face2d) | The `Face2D` class exposes details of a tracked face. |

