# ExternalTexture

The `ExternalTexture` class encapsulates a visual asset that is downloaded over the network.

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
      <td style="text-align:left">
        <p><code>(get) state: StringSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>StringSignal</code> representing the loading state of
          the external texture. The value of the signal is guaranteed to be a member
          of the <code>TexturesModule.ExternalTexture.State</code> enumeration.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>url</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) url: StringValue (set) url: StringSignal</code>
        </p>
        <p>Specifies the URL of the texture to be downloaded.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Enums

| Enum | Description |
| :--- | :--- |
| [`State`](https://sparkar.facebook.com/docs/ar-studio/reference/enums/texturesmodule.externaltexture.state) | The `State` enum describes the download state of an ExternalTexture. |

