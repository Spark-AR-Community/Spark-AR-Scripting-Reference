# Face2D

The `Face2D` class exposes details of a tracked face.

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
      <td style="text-align:left"><code>boundingBox</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) boundingBox: BoundingBoxSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>BoundingBoxSignal</code> object describing the face bounding
          box relative to normalized screen space.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>isTracked</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) isTracked: StringSignal (set) (Not Available)</code>
        </p>
        <p>A <code>boolSignal</code> indicating whether the face was tracked this frame.</p>
        <p>If the face was not tracked, other properties represent the most recent
          tracked frame.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

