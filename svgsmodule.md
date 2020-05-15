# SvgsModule

The `SvgsModule` module enables working with SVGs.

## Example

```text
//==============================================================================
// The following example demonstrates how to bind an SVG image to a vector
// object.
//
// Project setup:
// - Insert a vector object
//==============================================================================

// Load in the required modules
const Scene = require('Scene');
const Svgs = require('Svgs');

// Locate the SVG file in the Assets
const mySvg = Svgs.get('mySvg');

// Locate the vector object in the Scene
const vectorObject = Scene.root.find('vectorObject0');

// Bind the Svg to the vector object
vectorObject.svg = mySvg;
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
      <td style="text-align:left"><code>findFirst</code>
      </td>
      <td style="text-align:left">
        <p><code>findFirst(name: string): Promise&lt;Svg&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the svg of a requested name or
          null if none was found. <b>See Also</b>: <code>Svgs.findUsingPattern</code>, <code>Svgs.getAll</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>findUsingPattern</code>
      </td>
      <td style="text-align:left">
        <p><code>findUsingPattern(namePattern: string): Promise&lt;Array&lt;Svg&gt;&gt; findUsingPattern(namePattern: string, config: {limit: number}): Promise&lt;Array&lt;Svg&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the all of the svgs matching the
          name pattern or empty array if none was found.</p>
        <p>Pattern format: <code>*</code> matches any characters sequence. <code>\</code> can
          be used to include in pattern any of the control characters (including
          &apos;\&apos; itself)</p>
        <p>Examples: <code>findUsingPattern(&quot;*&quot;)</code> will retrive all
          of the svgs. <code>findUsingPattern(&quot;*A&quot;)</code> will retrieve
          all of the svgs suffixed with &apos;A&apos;. <code>findUsingPattern(&quot;A*&quot;)</code> will
          retrieve all of the svgs prefixed with &apos;A&apos;. <code>findUsingPattern(&quot;*A*&quot;, {limit: 10})</code> will
          retrieve at most 10 of the svgs containing &apos;A&apos;,</p>
        <p><code>limit</code> parameter describes if <code>findUsingPattern</code> should
          finish the search if it finds specified number of results (default is no
          limit). Non-positive values for limit are treated as unlimited.</p>
        <p><b>See Also</b>: <code>Svgs.getAll</code>, <code>Svgs.findFirst</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>get</code>
      </td>
      <td style="text-align:left">
        <p><code>get(svgName: string): Svg</code>
        </p>
        <p>Returns a svg object identified by the <code>svgName</code> argument.</p>
        <p>Throws an exception if there is no such identifier in the project.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>getAll</code>
      </td>
      <td style="text-align:left">
        <p><code>getAll(): Promise&lt;Array&lt;Svg&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with all of the svgs. <b>See Also</b>: <code>Svgs.findUsingPattern</code>, <code>Svgs.findFirst</code>.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`Svg`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/svgsmodule.svg) | The `Svg` class describes an SVG in an effect. |

