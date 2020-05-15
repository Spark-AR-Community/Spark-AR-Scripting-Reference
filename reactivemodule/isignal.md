# ISignal

The `ISignal` interface. The base class for `ScalarSignal`, `PointSignal`, `VectorSignal`, `BooleanSignal`, and `StringSignal`

## Properties

This module exposes no properties.

## Methods

<table>
  <thead>
    <tr>
      <th style="text-align:left">Method</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>valueOf</code>
      </td>
      <td style="text-align:left">
        <p><code>valueOf(): void</code>
        </p>
        <p>Throws an error. Signals are not supposed to be implicitly converted to
          scalar values.</p>
        <p><b>See also</b>: <code>ScalarSignal.add</code>, <code>ScalarSignal.sub</code>, <code>ScalarSignal.mul</code>, <code>ScalarSignal.div</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>