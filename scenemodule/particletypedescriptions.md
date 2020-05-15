# ParticleTypeDescriptions

The `ParticleTypeDescriptions` class provides a container for particle type descriptions.

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
      <td style="text-align:left"><code>count</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) count: number (set) (Not Available)</code>
        </p>
        <p>Retrieves the number of existing Particle Type Descriptions.</p>
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
      <td style="text-align:left"><code>get</code>
      </td>
      <td style="text-align:left">
        <p><code>get(index: number): ParticleTypeDescription</code>
        </p>
        <p>Retrieves the particle type description at that index. The particle type
          descriptions specify which frames of the sprite sheet the particle should
          use. From scripting, the frames that the ParticleTypeDescription is using
          cannot be changed, but the user can change their percentages, i.e if there
          are 2 particle types, with percentages 0.5 each, the user can change from
          scripting to make one particle type more dense than the other by changing
          their fractions, for example to 0.3 and 0.7 respectively.</p>
      </td>
    </tr>
  </tbody>
</table>