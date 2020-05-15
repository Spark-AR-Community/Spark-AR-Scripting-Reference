# DefaultMaterial

The `DefaultMaterial` class encapsulates an image-based material.

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
      <td style="text-align:left"><code>blendMode</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) blendMode: Signal&lt;MaterialsModule.BlendMode&gt; (set) blendMode: Signal&lt;MaterialsModule.BlendMode&gt;</code>
        </p>
        <p>Specifies the material blend mode.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>emissive</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) emissive: TextureBase (set) emissive: TextureBase</code>
        </p>
        <p>Specifies the emissive texture of the material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>emissiveTextureTransform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) emissiveTextureTransform: TextureTransform (set) emissiveTextureTransform: TextureTransformSignal</code>
        </p>
        <p>Specifies the coordinates transform of the emissive texture of this material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>multiply</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) multiply: TextureBase (set) multiply: TextureBase</code>
        </p>
        <p>Specifies the multiplicative texture of the material. This can be used
          for masking and other purposes.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>multiplyTextureTransform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) multiplyTextureTransform: TextureTransform (set) multiplyTextureTransform: TextureTransformSignal</code>
        </p>
        <p>Specifies the coordinates transform of the multiplicative texture of this
          material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>reflective</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) reflective: TextureBase (set) reflective: TextureBase</code>
        </p>
        <p>Specifies the reflective texture of the material.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

