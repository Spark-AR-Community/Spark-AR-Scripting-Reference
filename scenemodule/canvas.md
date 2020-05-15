# Canvas

The `Canvas` class describes a scene canvas.

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
      <td style="text-align:left"><code>bounds</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) bounds: Bounds2D (set) (Not Available)</code>
        </p>
        <p>Represents the current 2D bounds relative to the parent element. This
          is the result of the layout calculation. Values are measured in 3D units.</p>
        <p><b>Note</b>: The <code>Canvas.transform</code> property doesn&apos;t affect
          the layout, the transformation it specifies is applied on top of it.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>height</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) height: ScalarSignal (set) height: ScalarSignal</code>
        </p>
        <p>Specifies the vertical size, in 3D units. <b>Note:</b> this is only effective
          when <code>renderMode</code> property is set to WORLD_SPACE.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>renderMode</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) renderMode: SceneModule.RenderMode (set) renderMode: SceneModule.RenderMode</code>
        </p>
        <p>Specifies how Canvas should be rendered. In SCREEN_SPACE mode, Canvas
          is automatically placed and sized to fit the screen, <code>width</code> and <code>height</code> properties
          are ignored. <code>transform</code> property is still used, it is applied
          on top of the focal plane transform. In WORLD_SPACE Canvas behaves as regular
          3D object and is sized according to <code>width</code> and <code>height</code> properties.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>useSafeAreaMargins</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) useSafeAreaMargins: BoolSignal (set) useSafeAreaMargins: BoolSignal</code>
        </p>
        <p>Specifies if Canvas should automatically include SafeArea margin to its
          content. <b>Note:</b> this is only effective when <code>renderMode</code> property
          is set to SCREEN_SPACE.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>width</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) width: ScalarSignal (set) width: ScalarSignal</code>
        </p>
        <p>Specifies the horizontal size, in 3D units. <b>Note:</b> this is only effective
          when <code>renderMode</code> property is set to WORLD_SPACE.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

