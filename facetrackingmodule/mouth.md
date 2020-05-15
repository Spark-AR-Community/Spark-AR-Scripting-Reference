# Mouth

The `Mouth` class exposes the details of a detected mouth.

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
        <p>Specifies a <code>PointSignal</code> representing the location of the center
          of the mouth in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>leftCorner</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) leftCorner: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PointSignal</code> representing the location of the left
          corner of the mouth in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lowerLipCenter</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) lowerLipCenter: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PointSignal</code> representing the location of the center
          of the lower lip in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>lowerLipCurvature</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) lowerLipCurvature: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> indicating how high or low the mouth
          angles are with respect to the lip center. 0.0 is a straight line. Mouth
          angles higher than the lip center yield positive curvature, lowering the
          mouth angles makes it negative.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>openness</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) openness: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> representing the openness of the mouth.
          The openness of the mouth is a non-negative value where 0.0 is mouth closed
          and 1.0 mouth wide open (it can also take values greater than 1.0).</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rightCorner</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) rightCorner: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PointSignal</code> representing the location of the right
          corner of the mouth in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>upperLipCenter</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) upperLipCenter: PointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PointSignal</code> representing the location of the center
          of the upper lip in the face local coordinate system.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>upperLipCurvature</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) upperLipCurvature: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> indicating how high or low the mouth
          angles are with respect to the lip center. 0.0 is a straight line. Mouth
          angles higher than the lip center yield positive curvature, lowering the
          mouth angles makes it negative.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

