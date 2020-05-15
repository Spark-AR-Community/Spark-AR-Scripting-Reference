# FontsModule

The `FontsModule` class is used for working with custom fonts in effects.

## Example

```text
//==============================================================================
// The following example demonstrates how to access a font in the Assets and
// assign it to a text object.
//
// Project setup:
// - Insert text
// - Add the Custom Fonts capability
//==============================================================================

// Load in the required modules
const Fonts = require('Fonts');
const Scene = require('Scene');

// Locate the font in the Assets and the text in the Scene
const font = Fonts.get('customFont.ttf');
const text = Scene.root.find('text0');

// Set the font of the text
text.font = font;
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
        <p><code>findFirst(name: string): Promise&lt;FontId&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the font identifier of a requested
          name or null if none was found. <b>See Also</b>: <code>FontsModule.findUsingPattern</code>, <code>FontsModule.getAll</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>findUsingPattern</code>
      </td>
      <td style="text-align:left">
        <p><code>findUsingPattern(namePattern: string): Promise&lt;Array&lt;FontId&gt;&gt; findUsingPattern(namePattern: string, config: {limit: number}): Promise&lt;Array&lt;FontId&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the all of the font identifiers
          matching the name pattern or empty array if none was found.</p>
        <p>Pattern format: <code>*</code> matches any characters sequence. <code>\</code> can
          be used to include in pattern any of the control characters (including
          &apos;\&apos; itself)</p>
        <p>Examples: <code>findUsingPattern(&quot;*&quot;)</code> will retrive all
          of the font identifiers. <code>findUsingPattern(&quot;*A&quot;)</code> will
          retrieve all of the font identifiers suffixed with &apos;A&apos;. <code>findUsingPattern(&quot;A*&quot;)</code> will
          retrieve all of the font identifiers prefixed with &apos;A&apos;. <code>findUsingPattern(&quot;*A*&quot;, {limit: 10})</code> will
          retrieve at most 10 of the font identifiers containing &apos;A&apos;,</p>
        <p><code>limit</code> parameter describes if <code>findUsingPattern</code> should
          finish the search if it finds specified number of results (default is no
          limit). Non-positive values for limit are treated as unlimited.</p>
        <p><b>See Also</b>: <code>FontsModule.getAll</code>, <code>FontsModule.findFirst</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>get</code>
      </td>
      <td style="text-align:left">
        <p><code>get(fontName: string): FontId</code>
        </p>
        <p>Returns a font object identified by the <code>fontName</code> argument.</p>
        <p>Throws an exception if there is no such font in the project.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>getAll</code>
      </td>
      <td style="text-align:left">
        <p><code>getAll(): Promise&lt;Array&lt;FontId&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with all of the font identifiers. <b>See Also</b>: <code>FontsModule.findUsingPattern</code>, <code>FontsModule.findFirst</code>.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`FontId`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/fontsmodule.fontid) | The `FontsId` class identifies a font in an effect. |

