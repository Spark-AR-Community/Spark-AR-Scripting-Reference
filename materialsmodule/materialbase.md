# MaterialBase

The `MaterialBase` class exposes properties common to all material types.

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
      <td style="text-align:left"><code>alphaCutoff</code>
      </td>
      <td style="text-align:left"><code>(get) alphaCutoff: ScalarSignal (set) alphaCutoff: ScalarSignal</code> Specifies
        a number between 0.0 and 1.0.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>cullMode</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) cullMode: Signal&lt;MaterialsModule.CullMode&gt; (set) cullMode: Signal&lt;MaterialsModule.CullMode&gt;</code>
        </p>
        <p>Specifies the material cull mode.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>diffuse</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) diffuse: TextureBase (set) diffuse: TextureBase</code>
        </p>
        <p>Specifies the texture that forms the basis of this material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>diffuseTextureTransform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) diffuseTextureTransform: TextureTransform (set) diffuseTextureTransform: TextureTransformSignal</code>
        </p>
        <p>Specifies the coordinates transform of the diffuse texture of this material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>doubleSided</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) doubleSided: BoolSignal (set) doubleSided: BoolSignal</code>
        </p>
        <p>Indicates whether the material can be seen from both sides when rendering
          the scene.</p>
        <p><b>Note</b>: When <code>FALSE</code>, only the side specified by object&apos;s <b>Cull Mode</b> is
          rendered.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>identifier</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) identifier: string (set) (Not Available)</code>
        </p>
        <p>Specifies the unique identifier for the material.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>name</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) name: string (set) (Not Available)</code>
        </p>
        <p>Specifies the unique identifier for the material name. This value is specified
          in AR Studio at design time.</p>
        <p><b>See Also</b>: <code>MaterialsModule.get</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>opacity</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) opacity: ScalarSignal (set) opacity: ScalarSignal</code>
        </p>
        <p>Specifies a number between 0.0 and 1.0 indicating the opacity threshold
          for discarding pixels. 0 is transparent and 1 is opaque.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>setTexture</code>
      </td>
      <td style="text-align:left">
        <p><code>setTexture(signal: ShaderSignal, config: { textureSlotName: DefaultMaterialTextures | BlendedMaterialTextures | FacePaintMaterialTextures | PhysicallyBasedMaterialTextures }): void</code>
        </p>
        <p>Assigns a <code>ShaderSignal</code> to the specified texture slot.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>setTextureSlot</code>
      </td>
      <td style="text-align:left">
        <p><code>setTextureSlot(textureSlotName: String, signal: ShaderSignal): void</code>
        </p>
        <p>Assigns a <code>ShaderSignal</code> to the specified texture slot.</p>
      </td>
    </tr>
  </tbody>
</table>