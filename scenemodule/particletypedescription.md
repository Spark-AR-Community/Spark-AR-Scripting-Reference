# ParticleTypeDescription

The `ParticleTypeDescription` class provides functionality for setting particle sprite densities in the scene.

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
      <td style="text-align:left"><code>fraction</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) fraction: ScalarValue (set) fraction: ScalarSignal</code>
        </p>
        <p>The fraction of particles, that should be of that ParticleTypeDescription.
          This is thought to be used for making the sorting better between different
          particles. The user can specify the fraction of particles that can use
          the specific frames of one sprite sheet (which is specified from the UI),
          which would make sorting of different particles proper.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

