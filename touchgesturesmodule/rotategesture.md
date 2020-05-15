# RotateGesture

The `RotateGesture` class contains the details of a detected rotate gesture.

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
      <td style="text-align:left"><code>location</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) location: PixelPointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/pixelpointsignal_class"><code>PixelPointSignal</code></a> object
          that represents the center point between two touches in screen coordinates.</p>
        <p><b>Note</b>: The location is always specified in the screen coordinates,
          even if the event was emitted as a result of rotating on a specific object.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>rotation</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) rotation: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/scalarsignal_class"><code>ScalarSignal</code></a> representing
          the rotation indicated by the gesture, in radians.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

