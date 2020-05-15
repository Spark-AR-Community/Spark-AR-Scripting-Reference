# TextureBase

The `TextureBase` class describes a texture.

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
      <td style="text-align:left"><code>height</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) height: ScalarSignal</code>
        </p>
        <p>Gets the height of the texture in pixels.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>identifier</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) identifier: StringValue (set) (Not Available)</code>
        </p>
        <p>Specifies the unique texture identifier. This value is specified internally
          in AR Studio.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>name</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) name: StringValue (set) (Not Available)</code>
        </p>
        <p>Specifies the unique texture name. The texture name is specified in AR
          Studio at design time.</p>
        <p><b>See Also</b>: <code>TexturesModule.get</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>signal</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) signal: ShaderSignal</code>
        </p>
        <p>Gets the RGBA ShaderSignal of the given texture. This signal can then
          be used in shader computations.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>width</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) width: ScalarSignal</code>
        </p>
        <p>Gets the width of the texture in pixels.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

