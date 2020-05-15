# PanGesture

The `PanGesture` class contains the details of a detected pan gesture.

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
        <p>Specifies a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/pixelpointsignal_class"><code>PixelPointSignal</code></a> that
          represents the location of the gesture in screen coordinates.</p>
        <p><b>Note</b>: The location is always specified in the screen coordinates,
          even if the event was emitted as a result of panning on a specific object.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>translation</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) translation: PixelPointSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/pixelpointsignal_class"><code>PixelPointSignal</code></a> indicating
          the position of the gesture, in screen coordinates, relative to the start
          point.</p>
        <p><b>Note</b>: The translation is always specified in the screen coordinates,
          even if the event was emitted as a result of panning on a specific object.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

