# StringValue

The `StringValue` class contains a string value.

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
      <td style="text-align:left"><code>lastValue</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) lastValue: string (set) (Not Available)</code>
        </p>
        <p>Specifies a string representing the last value of the object.</p>
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
      <td style="text-align:left"><code>pinLastValue</code>
      </td>
      <td style="text-align:left">
        <p><code>pinLastValue(): ConstStringSignal</code>
        </p>
        <p>Returns a <code>ConstStringSignal</code> containing a constant value which
          is the last value of the specified signal before <code>pinLastValue</code> is
          called. ConstStringSignal can be passed to a functions which accept strings.</p>
      </td>
    </tr>
  </tbody>
</table>