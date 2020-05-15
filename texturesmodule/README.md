# TexturesModule

The `TexturesModule` class enables images, animation sequences, videos, colors, and other visual artifacts to be combined to form materials.

## Example

```text
//==============================================================================
// The following example demonstrates how to access a texture in the Assets and
// assign it to a material.
//
// Project setup:
// - Insert a plane
// - Create a material
// - Import an image to use as a texture (renaming it texture0)
// - Assign the material to the plane
//==============================================================================

// Load in the required modules
const Materials = require('Materials');
const Textures = require('Textures');

// Locate the material and texture in the Assets
const material = Materials.get('defaultMaterial0');
const texture = Textures.get('texture0');

// Assign the texture to the material
material.diffuse = texture;
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
        <p><code>findFirst(name: string): Promise&lt;TextureBase&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the texture of a requested name
          or null if none was found.</p>
        <p><b>See Also</b>: <code>Textures.findUsingPattern</code>, <code>Textures.getAll</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>findUsingPattern</code>
      </td>
      <td style="text-align:left">
        <p><code>findUsingPattern(namePattern: string): Promise&lt;Array&lt;TextureBase&gt;&gt; findUsingPattern(namePattern: string, config: {limit: number}): Promise&lt;Array&lt;TextureBase&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the all of the textures matching
          the name pattern or empty array if none was found.</p>
        <p>Pattern format: <code>*</code> matches any characters sequence. <code>\</code> can
          be used to include in pattern any of the control characters (including
          &apos;\&apos; itself)</p>
        <p>Examples: <code>findUsingPattern(&quot;*&quot;)</code> will retrive all
          of the textures. <code>findUsingPattern(&quot;*A&quot;)</code> will retrieve
          all of the textures suffixed with &apos;A&apos;. <code>findUsingPattern(&quot;A*&quot;)</code> will
          retrieve all of the textures prefixed with &apos;A&apos;. <code>findUsingPattern(&quot;*A*&quot;, {limit: 10})</code> will
          retrieve at most 10 of the textures containing &apos;A&apos;,</p>
        <p><code>limit</code> parameter describes if <code>findUsingPattern</code> should
          finish the search if it finds specified number of results (default is no
          limit). Non-positive values for limit are treated as unlimited.</p>
        <p><b>See Also</b>: <code>Textures.getAll</code>, <code>Textures.findFirst</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>get</code>
      </td>
      <td style="text-align:left">
        <p><code>get(textureName: string): TextureBase</code>
        </p>
        <p>Returns a texture object, derived from <code>TextureBase</code>, that is
          specified by <code>textureName</code>. An exception is thrown when the texture
          isn&apos;t found in the project. Possible types are:</p>
        <ul>
          <li><code>CanvasTexture</code>
          </li>
          <li><code>ColorTexture</code>
          </li>
          <li><code>DeepLinkTexture</code>
          </li>
          <li><code>ExternalTexture</code>
          </li>
          <li><code>ImageTexture</code>
          </li>
          <li><code>SequenceTexture</code>
          </li>
        </ul>
        <p><b>See Also</b>: <code>TextureBase.name</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>getAll</code>
      </td>
      <td style="text-align:left">
        <p><code>getAll(): Promise&lt;Array&lt;TextureBase&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with all of the textures.</p>
        <p><b>See Also</b>: <code>Textures.findUsingPattern</code>, <code>Textures.findFirst</code>.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

| Class | Description |
| :--- | :--- |
| [`CameraTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.cameratexture) | The `CameraTexture` class. |
| [`CanvasTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.canvastexture) | The `CanvasTexture` class enables painting with a brush to a texture. |
| [`ColorTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.colortexture) | The `ColorTexture` class encapsulates a texture that has a color \(including alpha channel\). |
| [`DeepLinkTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.deeplinktexture) | The `DeepLinkTexture` class represents an image texture passed in via the sharing SDK. |
| [`ExternalTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.externaltexture) | The `ExternalTexture` class encapsulates a visual asset that is downloaded over the network. |
| [`ImageTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.imagetexture) | The `ImageTexture` class encapsulates an image that may be used to form materials for rendering in the scene. |
| [`SegmentationTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.segmentationtexture) | The `SegmentationTexture` class encapsulates a texture that will be used for image segmentation. |
| [`SequenceTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.sequencetexture) | The `SequenceTexture` class is a collection of still images that form an animation. |
| [`SourceImageRegionTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.sourceimageregiontexture) | The `SourceImageRegionTexture` class. |
| [`SubTexture`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.subtexture) | The `SubTexture` class exposes details of a texture in UV coordinates. |
| [`TextureBase`](https://sparkar.facebook.com/docs/ar-studio/reference/classes/texturesmodule.texturebase) | The `TextureBase` class describes a texture. |

