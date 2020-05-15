# BoolValue

The `BoolValue` class contains a Boolean value.

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
        <p><code>(get) lastValue: boolean (set) (Not Available)</code>
        </p>
        <p>Specifies a Boolean representing the last value of the object.</p>
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
        <p><code>pinLastValue(): ConstBoolSignal</code>
        </p>
        <p>Returns a <code>ConstBoolSignal</code> containing a constant value which
          is the last value of the specified signal before <code>pinLastValue</code> is
          called. ConstBoolSignal can be passed to a functions which accept bools.</p>
      </td>
    </tr>
  </tbody>
</table>