# Speaker

The `Speaker` class encapsulates an speaker for a scene. Old class name is `AudioSource`.

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
      <td style="text-align:left"><code>volume</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) volume: ScalarValue (set) volume: ScalarSignal</code>
        </p>
        <p>(get) Returns the volume of the speaker in the range of [0.0, 1.0]. (set)
          Specifies the volume of the speaker in the range of [0.0, 1.0].</p>
        <p>Note: To access this property you need to enable the AudioSourceVolume
          API capability.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>play</code>
      </td>
      <td style="text-align:left">
        <p><code>play(): void</code>
        </p>
        <p>Creates a new playing instance of the sound associated with this AudioSource.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>stopAll</code>
      </td>
      <td style="text-align:left">
        <p><code>stopAll(speaker: Speaker): void</code>
        </p>
        <p>Stops all playing instances of this AudioSource.</p>
      </td>
    </tr>
  </tbody>
</table>