# DeepLinkModule

The `DeepLinkModule` class exposes methods and properties to read the values that an external app sent to an effect.

## Example

```text
//==============================================================================
// The following example demonstrates how to retrieve data passed in to an
// effect from an external app.
//
// Note: This example is based on an external app sending a 'name' argument.
//==============================================================================

// Load in the required modules
const DeepLink = require('DeepLink');
const Diagnostics = require('Diagnostics');

// Store a reference to the name argument passed from an external app
let name = DeepLink.arguments.name;

// If the name argument does not exist then set a default value
if (!name) {
    name = 'Jane Doe';
}

// Log the name
Diagnostics.log(name);
```

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
      <td style="text-align:left"><code>arguments</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) arguments: { [key: string]: Object} (set) (Not Available)</code>
        </p>
        <p>Specifies a collection of key/value pairs passed from the external app.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Classes

This module exposes no classes.

