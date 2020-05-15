# PinchGesture

The `PinchGesture` class contains the details of a detected pinch gesture.

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
        <p><code>(get) location: PixelPointSignal (set) (Not Available)</code> Specifies
          a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/pixelpointsignal_class"><code>PixelPointSignal</code></a> that
          represents the current center point between two touches of the pinch gesture
          in screen coordinates.</p>
        <p><b>Note</b>: The location is always specified in the screen coordinates,
          even if the event was emitted as a result of pinching on a specific object.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>scale</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) scale: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/scalarsignal_class"><code>ScalarSignal</code></a> representing
          the scale factor indicated by the gesture.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

