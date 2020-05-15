# MaterialsModule

The `Materials` module provides access to the materials in an effect.

## Example

```text
//==============================================================================
// The following example demonstrates how to access a material in the Assets,
// assign it to an object, and change it's opacity.
//
// Project setup:
// - Insert a plane
// - Create a material
//==============================================================================

// Load in the required modules
const Materials = require('Materials');
const Scene = require('Scene');

// Locate the plane in the Scene
const plane = Scene.root.find('plane0');

// Locate the plane in the Scene
const material = Materials.get('defaultMaterial0');

// Assign the material to the plane
plane.material = material;

// Set the opacity of the material to 50%
material.opacity = 0.5;
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
        <p><code>findFirst(name: string): Promise&lt;MaterialBase&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the material of a requested name
          or null if none was found.</p>
        <p><b>See Also</b>: <code>Materials.findUsingPattern</code>, <code>Materials.getAll</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>findUsingPattern</code>
      </td>
      <td style="text-align:left">
        <p><code>findUsingPattern(namePattern: string): Promise&lt;Array&lt;MaterialBase&gt;&gt; findUsingPattern(namePattern: string, config: {limit: number}): Promise&lt;Array&lt;MaterialBase&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the all of the materials matching
          the name pattern or empty array if none was found.</p>
        <p>Pattern format: <code>*</code> matches any characters sequence. <code>\</code> can
          be used to include in pattern any of the control characters (including
          &apos;\&apos; itself)</p>
        <p>Examples: <code>findUsingPattern(&quot;*&quot;)</code> will retrive all
          of the materials. <code>findUsingPattern(&quot;*A&quot;)</code> will retrieve
          all of the materials suffixed with &apos;A&apos;. <code>findUsingPattern(&quot;A*&quot;)</code> will
          retrieve all of the materials prefixed with &apos;A&apos;. <code>findUsingPattern(&quot;*A*&quot;, {limit: 10})</code> will
          retrieve at most 10 of the materials containing &apos;A&apos;,</p>
        <p><code>limit</code> parameter describes if <code>findUsingPattern</code> should
          finish the search if it finds specified number of results (default is no
          limit). Non-positive values for limit are treated as unlimited.</p>
        <p><b>See Also</b>: <code>Materials.getAll</code>, <code>Materials.findFirst</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>get</code>
      </td>
      <td style="text-align:left">
        <p><code>get(materialName: string): MaterialBase</code>
        </p>
        <p>Returns a <code>MaterialBase</code> class that represents the material specified
          by the <code>materialName</code> parameter. The materials are defined in
          the AR Studio project.</p>
        <p>An exception is thrown when the identifier isn&apos;t found in the project.</p>
        <p><b>See Also</b>: <code>MaterialBase.name</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>getAll</code>
      </td>
      <td style="text-align:left">
        <p><code>getAll(): Promise&lt;Array&lt;MaterialBase&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with all of the materials.</p>
        <p><b>See Also</b>: <code>Materials.findUsingPattern</code>, <code>Materials.findFirst</code>.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`BlendedMaterial`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.blendedmaterial) | The `BlendedMaterial` class encapsulates materials blended from multiple textures. |
| [`BlendShapeToWarpMapMaterial`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.blendshapetowarpmapmaterial) | The `BlendShapeToWarpMapMaterial` class. |
| [`ColorPaintMaterial`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.colorpaintmaterial) | The `ColorPaintMaterial` class encapsulates a face-paint material. |
| [`ComposedMaterial`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.composedmaterial) | The `ComposedMaterial` class encapsulates patch asset materials. |
| [`DefaultMaterial`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.defaultmaterial) | The `DefaultMaterial` class encapsulates an image-based material. |
| [`MaterialBase`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.materialbase) | The `MaterialBase` class exposes properties common to all material types. |
| [`MetallicRoughnessPbrMaterial`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.metallicroughnesspbrmaterial) | The `MetallicRoughnessPbrMaterial` class encapsulates physically based materials. |
| [`RetouchingMaterial`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.retouchingmaterial) | The `RetouchingMaterial` class encapsulates parameters which define the extend of certain beautification techniques. |
| [`TextureTransform`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/materialsmodule.texturetransform) | The `TextureTransform` class encapsulates scaling and translation transforms about a textures UV axis. |

## Enums

| Enum | Description |
| :--- | :--- |
| [`BlendMode`](https://sparkar.facebook.com/docs/ar-studio/reference/enums/materialsmodule.blendmode) | The `BlendMode` enum describes how material is blended. |
| [`CullMode`](https://sparkar.facebook.com/docs/ar-studio/reference/enums/materialsmodule.cullmode) | The `CullMode` enum describes how material is culled. |

