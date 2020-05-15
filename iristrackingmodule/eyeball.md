# Eyeball

The `Eyeball` class exposes details of a tracked eyeball.

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
      <td style="text-align:left"><code>center</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) center: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies the 3D position of the center point of the eyeball in the face
          local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>iris</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) iris: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies the 3D position of the center point of the iris in the face
          local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rotation</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) rotation: RotationSignal (set) (Not Available)</code>
        </p>
        <p>Specifies the rotation of the eyeball around its center.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

