# Mesh

The `Mesh` class describes a scene mesh.

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
      <td style="text-align:left"><code>blendShapes</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) blendShapes: BlendShapesMesh (set) (Not Available)</code>
        </p>
        <p>Returns the set of blendshapes that this mesh contains.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>material</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) material: MaterialBase (set) material: MaterialBase</code>
        </p>
        <p>Specifies the material of the scene object.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>materialIdentifier</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) materialIdentifier: string (set) (Not Available)</code>
        </p>
        <p>Specifies the unique id of material for Mesh.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>prefabName</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) prefabName: string (set) (Not Available)</code>
        </p>
        <p>Specifies the name of prefab for Mesh. This is the unique identifier of
          the prefab.</p>
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
      <td style="text-align:left"><code>getBlendShapes</code>
      </td>
      <td style="text-align:left">
        <p><code>getBlendShapes(): Promise&lt;ArrayOfBlendShapes&gt;</code>
        </p>
        <p>Returns a <code>JS Promise</code> which will be fulfilled with <code>array of blend Shapes</code> or
          an error.</p>
      </td>
    </tr>
  </tbody>
</table>