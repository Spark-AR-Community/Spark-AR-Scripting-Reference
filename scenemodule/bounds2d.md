# Bounds2D

The `Bounds2D` class describes the bounds of a scene element.

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
      <td style="text-align:left"><code>height</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) height: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies the height of the scene element boundaries. Measured in 3D units.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>width</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) width: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies the width of the scene element boundaries. Measured in 3D units.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>x</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) x: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies the left boundary of the scene element. Relative to the parent
          object bounds. Measured in 3D units.</p>
        <p><b>Note</b>: the offset is measured from the parent&apos;s left boundary,
          which might be different from the parent&apos;s origin.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>y</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) y: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies the top boundary of the scene element. Relative to the parent
          object bounds. Measured in 3D units.</p>
        <p><b>Note</b>: the offset is measured from the parent&apos;s top boundary,
          which might be different from the parent&apos;s origin.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

