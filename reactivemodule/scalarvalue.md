# ScalarValue

The `ScalarValue` class contains a scalar value.

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
        <p><code>(get) lastValue: number (set) (Not Available)</code>
        </p>
        <p>Specifies a number representing the last value of the object.</p>
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
        <p><code>pinLastValue(): ConstScalarSignal</code>
        </p>
        <p>Returns a <code>ConstScalarSignal</code> containing a constant value which
          is the last value of the specified signal before <code>pinLastValue</code> is
          called. ConstScalarSignal can be passed to a functions which accept numbers.</p>
      </td>
    </tr>
  </tbody>
</table>