# Gesture

The `Gesture` class encapsulates details of a detected gesture.

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
      <td style="text-align:left"><code>state</code>
      </td>
      <td style="text-align:left"><code>(get) state: StringSignal (set) (Not Available)</code> Specifies
        a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/reactive_module/stringsignal_class"><code>StringSignal</code></a> representing
        the current gesture state. The value is a member of the <a href="https://sparkar.facebook.com/docs/camera-effects/reference/gesture_state_enum"><code>Gesture.State</code></a> enum.</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) type: Gesture.Type (set) (Not Available)</code>
        </p>
        <p>Specifies a <a href="https://sparkar.facebook.com/docs/camera-effects/reference/type_enum"><code>Gesture.Type</code></a> enum
          value representing the type of gesture detected.</p>
        <p>To use this property, enable pre-release APIs in your project manifest.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Enums

| Enum | Description |
| :--- | :--- |
| [`State`](https://sparkar.facebook.com/docs/ar-studio/reference/enums/touchgesturesmodule.gesture.state) | The State enum describes the state of a Gesture. |
| [`Type`](https://sparkar.facebook.com/docs/ar-studio/reference/enums/touchgesturesmodule.gesture.type) | The `Type` enum describes a touch gesture. |

