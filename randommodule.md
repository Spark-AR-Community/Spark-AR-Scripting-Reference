# RandomModule

The `RandomModule` class enables random number generation.

## Example

```text
//==============================================================================
// The following example demonstrates how to generate a random number and use it
// to change the scale of an object.
//
// Project setup:
// - Insert a plane
//==============================================================================

// Load in the required modules
const Random = require('Random');
const Scene = require('Scene');

// Locate the plane in the Scene
const plane = Scene.root.find('plane0');

// Store a random number
const randomNum = Random.random();

// Bind the random number to the x-axis scale signal of the plane
plane.transform.scaleX = randomNum;
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
      <td style="text-align:left"><code>random</code>
      </td>
      <td style="text-align:left">
        <p><code>random(): number</code>
        </p>
        <p>Returns a uniformly distributed number between 0.0 (inclusive) and 1.0
          (exclusive).</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

This module exposes no classes.

