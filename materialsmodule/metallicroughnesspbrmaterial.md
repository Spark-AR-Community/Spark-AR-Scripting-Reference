# MetallicRoughnessPbrMaterial

The `MetallicRoughnessPbrMaterial` class encapsulates physically based materials.

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
      <td style="text-align:left"><code>baseColor</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) (Not Available) (set) baseColor: TextureBase</code>
        </p>
        <p>Specifies the baseColor texture of the material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>baseColorFactor</code>
      </td>
      <td style="text-align:left"><code>(get) (Not Available) (set) baseColorFactor: ColorSignal</code> Specifies
        a <code>ColorSignal</code> for a base color factor. A <code>ColorSignal</code> may
        be created using the <code>RGBA()</code> and <code>HSVA()</code> methods of
        the <code>Reactive</code> module. <b>See Also</b>: <code>ReactiveModule.RGBA</code> and <code>ReactiveModule.HSVA</code>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>baseColorTextureTransform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) baseColorTextureTransform: TextureTransform (set) baseColorTextureTransform: TextureTransformSignal</code>
        </p>
        <p>Specifies the coordinates transform of the baseColorFactor texture of
          this material.</p>
      </td>
    </tr>
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
      <td style="text-align:left"><code>metallicFactor</code>
      </td>
      <td style="text-align:left"><code>(get) metallicFactor: ScalarSignal (set) metallicFactor: ScalarSignal</code> Specifies
        the metallic factor.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>metallicRoughness</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) (Not Available) (set) metallicRoughness: TextureBase</code>
        </p>
        <p>Specifies the metallicRoughness texture of the material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>metallicRoughnessTextureTransform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) metallicRoughnessTextureTransform: TextureTransform (set) metallicRoughnessTextureTransform: TextureTransformSignal</code>
        </p>
        <p>Specifies the coordinates transform of the metallicRoughness texture of
          this material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>roughnessFactor</code>
      </td>
      <td style="text-align:left"><code>(get) roughnessFactor: ScalarSignal (set) roughnessFactor: ScalarSignal</code> Specifies
        the roughness factor.</td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

