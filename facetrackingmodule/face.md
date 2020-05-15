# Face

The `Face` class exposes details of a tracked face.

### Properties

<table>
  <thead>
    <tr>
      <th style="text-align:left">Property</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>cameraTransform</code>
      </td>
      <td style="text-align:left">
        <p>Specifies a <code>TransformSignal</code> object describing the face transformation
          relative to camera coordinate system.</p>
        <p><b>Note</b>: <code>cameraTransform.applyTo(point)</code>, where <code>point</code> is
          a point in face local coordinate system, returns a point in camera local
          coordinate system.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>chin</code>
      </td>
      <td style="text-align:left">Specifies a <code>Chin</code> object describing the attributes of the chin.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>forehead</code>
      </td>
      <td style="text-align:left">Specifies a <code>Forehead</code> object describing the attributes of the
        forehead.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>id</code>
      </td>
      <td style="text-align:left">
        <p>Specifies a <code>StringSignal</code> containing the unique ID assigned
          to a face. An ID is generated every time a face is detected and tracked
          in the scene.</p>
        <p>When a face is lost and then tracked again, a new ID is generated even
          if it is the same person.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>isTracked</code>
      </td>
      <td style="text-align:left">
        <p>A <code>boolSignal</code> indicating whether the face was tracked this frame.</p>
        <p>If the face was not tracked, other properties represent the most recent
          tracked frame.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>leftCheek</code>
      </td>
      <td style="text-align:left">Specifies a <code>Cheek</code> object describing the attributes of the left
        cheek.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>leftEye</code>
      </td>
      <td style="text-align:left">Specifies an <code>Eye</code> object describing the attributes of the left
        eye.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>leftEyebrow</code>
      </td>
      <td style="text-align:left">Specifies an <code>Eyebrow</code> object describing the attributes of the
        left eyebrow.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>mouth</code>
      </td>
      <td style="text-align:left">Specifies a <code>Mouth</code> object describing the attributes of the mouth.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>nose</code>
      </td>
      <td style="text-align:left">Specifies a <code>Nose</code> object describing the attributes of the nose.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rightCheek</code>
      </td>
      <td style="text-align:left">Specifies a <code>Cheek</code> object describing the attributes of the right
        cheek.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rightEye</code>
      </td>
      <td style="text-align:left">Specifies an <code>Eye</code> object describing the attributes of the right
        eye.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rightEyebrow</code>
      </td>
      <td style="text-align:left">Specifies an <code>Eyebrow</code> object describing the attributes of the
        right eyebrow.</td>
    </tr>
  </tbody>
</table>### Methods

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>point</code>
      </td>
      <td style="text-align:left">
        <p>Returns a <code>PointSignal</code> object representing a point in the face
          local coordinate system that corresponds to a UV point on the facial mesh
          texture map.</p>
        <p><b>See Also</b>: <code>Face.cameraTransform</code> to convert the point
          to the coordinate system of the camera.</p>
      </td>
    </tr>
  </tbody>
</table>