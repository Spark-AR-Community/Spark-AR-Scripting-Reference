# UnitsModule

The `UnitsModule` class provides functionality for converting values into world-space units.

## Example

```text
//==============================================================================
// The following example demonstrates how to convert values into world-space
// units.
//
// Project setup:
// - Set the default unit via Properties > General > Unit of Measurement
//==============================================================================

// Load in the required modules
const Diagnostics = require('Diagnostics');
const Units = require('Units');

// Create a variable we will use to convert
const value = 5;

// Convert the value into other units
Diagnostics.log(value + ' cm => ' + Units.cm(value));
Diagnostics.log(value + ' ft => ' + Units.ft(value));
Diagnostics.log(value + ' in => ' + Units.in(value));
Diagnostics.log(value + ' m => '  + Units.m(value));
Diagnostics.log(value + ' mm => ' + Units.mm(value));
Diagnostics.log(value + ' yd => ' + Units.yd(value));
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
      <td style="text-align:left"><code>cm</code>
      </td>
      <td style="text-align:left">
        <p><code>cm(centimeters: number): number</code>
        </p>
        <p>Converts the specified centimeter value to world units.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>ft</code>
      </td>
      <td style="text-align:left">
        <p><code>ft(feet: number): number</code>
        </p>
        <p>Converts the specified foot value to world units.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>in</code>
      </td>
      <td style="text-align:left">
        <p><code>in(inches: number): number</code>
        </p>
        <p>Converts the specified inch value to world units.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>m</code>
      </td>
      <td style="text-align:left">
        <p><code>m(meters: number): number</code>
        </p>
        <p>Converts the specified meter value to world units.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>mm</code>
      </td>
      <td style="text-align:left">
        <p><code>mm(millimeters: number): number</code>
        </p>
        <p>Converts the specified millimeter value to world units.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>yd</code>
      </td>
      <td style="text-align:left">
        <p><code>yd(yards: number): number</code>
        </p>
        <p>Converts the specified yard value to world units.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

This module exposes no classes.

