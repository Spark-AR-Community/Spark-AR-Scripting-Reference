# LightingEstimationModule

The `LightingEstimation` module encapsulates access to estimations of lighting in the scene.

## Example

```text
//==============================================================================
// The following example demonstrates how to bind the frame brightness property
// to the intensity of a light.
//
// Project setup:
// - Insert a plane
// - Add the 'Frame Brightness' capability
// - (Recommended) Remove the directional light
//==============================================================================

// Load in the required modules
const LightingEstimation = require('LightingEstimation');
const Reactive = require('Reactive');
const Scene = require('Scene');

// Locate the ambientLight in the Scene
const ambientLight = Scene.root.find('ambientLight0');

// Calculate light intensity by subtracting the frame brightness from 1, the
// darker the frame brightness, the greater the light intensity
const lightIntensity = Reactive.sub(1,LightingEstimation.frameBrightness);

// Bind the light intensity to the intensity of the ambient light
ambientLight.intensity = lightIntensity;
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
      <td style="text-align:left"><code>frameBrightness</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) frameBrightness: ScalarSignal</code>
        </p>
        <p>Specifies a number that represents the brightness of the frame.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Classes

This module exposes no classes.

