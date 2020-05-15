# TextExtrusion

The `TextExtrusion` class describes a 3D text scene object.

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
      <td style="text-align:left"><code>backMaterial</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) (Not Available) (set) backMaterial: MaterialBase</code>
        </p>
        <p>Specifies the material of the back cap of 3-d text.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>depth</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) depth: ScalarSignal (set) depth: ScalarSignal</code>
        </p>
        <p>Text extrusion is only made through straight paths. This specifies the
          depth of the straight path of extrusion, starting from the position of
          textExtrusion scene object.</p>
        <p><b>Note</b>: Default value is 10 mm.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>faceMaterial</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) (Not Available) (set) faceMaterial: MaterialBase</code>
        </p>
        <p>Specifies the material of the caps or face of 3-d text.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>font</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) (Not Available) (set) font: FontId</code>
        </p>
        <p>Sets the given font from the fonts registry.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>frontMaterial</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) (Not Available) (set) frontMaterial: MaterialBase</code>
        </p>
        <p>Specifies the material of the front cap of 3-d text.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>letterSpacing</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) letterSpacing: ScalarSignal (set) letterSpacing: ScalarSignal</code>
        </p>
        <p>Specifies the letter spacing value.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lineSpacing</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) lineSpacing: ScalarSignal (set) lineSpacing: ScalarSignal</code>
        </p>
        <p>Specifies the line spacing value.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>sideMaterial</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) (Not Available) (set) sideMaterial: MaterialBase</code>
        </p>
        <p>Specifies the material of the extrusion part of 3-d text.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>text</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) text: StringSignal (set) text: StringSignal</code>
        </p>
        <p>Specifies the text displayed.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

