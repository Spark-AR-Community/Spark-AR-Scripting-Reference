# Eye

The `Eye` class exposes the details of a detected eye.

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
        <p>Specifies a <code>PointSignal</code> representing the center of the eye
          in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>insideCorner</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) insideCorner: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PointSignal</code> representing the inside corner of the
          eye in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lowerEyelidCenter</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) lowerEyelidCenter: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PointSignal</code> representing the center of the lower
          eyelid in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>openness</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) openness: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> representing the openness of the eye.
          The openness of the eye is a non-negative value where 0.0 is eye closed
          and 1.0 eye wide open (it can also take values greater than 1.0).</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>outsideCorner</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) outsideCorner: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PointSignal</code> representing the outside corner of
          the eye in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>upperEyelidCenter</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) upperEyelidCenter: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PointSignal</code> representing the center of the upper
          eyelid in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

