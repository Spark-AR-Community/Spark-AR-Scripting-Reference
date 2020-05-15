# PersonSegmentationModule

The `PersonSegmentationModule` class enables the separation of a person from a scene.

## Example

```text
//==============================================================================
// The following example demonstrates how to enable and disable segementation
// when detecting a person in the camera view as well as changing the opacity of
// a material depending on how close the person is to the camera.
//
// Project setup:
// - Follow the segmentation steps here (www.fb.me/spark-ar-using-segmentation)
//==============================================================================

// Load in the required modules
const Materials = require('Materials');
const PersonSegmentation = require('PersonSegmentation');
const Scene = require('Scene');

// Locate the rectangle and material in the Scene and Assets
const rectangle = Scene.root.find('rectangle0');
const rectangleMaterial = Materials.get('defaultMaterial0');

// Bind the foregroundPercent scalar signal to the opacity of the material
rectangleMaterial.opacity = PersonSegmentation.foregroundPercent;

// Bind the inverse of the hasForeground boolean signal to the hidden property
// of the rectangle
rectangle.hidden = PersonSegmentation.hasForeground.not();
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
      <td style="text-align:left"><code>foregroundPercent</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) foregroundPercent: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Represents the percentage of screen space occupied by a person/people.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>hasForeground</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) hasForeground: BoolSignal (set) (Not Available)</code>
        </p>
        <p>Represents whether there is anybody in the scene (TRUE/FALSE), based on
          whether the percentage of foreground is larger than a threshold.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>isEnabled</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) (Not Available) (set) isEnabled: BoolSignal</code>
        </p>
        <p>Specifies whether the segmentation should be enabled. Default value is
          &apos;true&apos;.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Classes

This module exposes no classes.

