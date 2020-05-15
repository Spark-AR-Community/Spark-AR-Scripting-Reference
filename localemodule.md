# LocaleModule

The `LocaleModule` class encapsulates access to the locale identifier of the device.

## Example

```text
//==============================================================================
// The following example demonstrates how to detect the device language and
// log a greeting in that language.
//==============================================================================

// Load in the required modules
const Diagnostics = require('Diagnostics');
const Locale = require('Locale');

// Store the unedited locale string (made up of the language_territory)
const languageAndTerritory = Locale.fromDevice;

// Log the locale string to the Console
Diagnostics.log('My location and territory are ' + languageAndTerritory);

// Create an array by splitting the locale string, this array will have two
// values, the language [0] and the territory [1]
const localeAsArray = languageAndTerritory.split('_');

// Store the first element in the array (the language)
const language = localeAsArray[0];

// Use a switch statement to say hello in the Console in the correct language
switch (language) {
  // English
  case 'en':
    Diagnostics.log('Hello');
    break;
  // Spanish
  case 'es':
    Diagnostics.log('Hola');
    break;
  // French
  case 'fr':
    Diagnostics.log('Bonjour');
    break;
  // Other
  default:
    Diagnostics.log('Device language is neither English, Spanish nor French');
    break;
}
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
      <td style="text-align:left"><code>fromDevice</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) fromDevice: string (set) (Not Available)</code>
        </p>
        <p>Provides the ISO 639-1 language + ISO 3166-1 region compliant locale identifier,
          e.g. <code>en_US</code> or <code>zh_HK</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>language</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) language: StringSignal (set) (Not Available)</code>
        </p>
        <p>Provides the ISO 639-1 compliant language identifier, e.g. <code>en</code> or <code>zh</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>locale</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) locale: StringSignal (set) (Not Available)</code>
        </p>
        <p>Provides the ISO 639-1 language + ISO 3166-1 region compliant locale identifier,
          e.g. <code>en_US</code> or <code>zh_HK</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>region</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) region: StringSignal (set) (Not Available)</code>
        </p>
        <p>Provides the ISO 3166-1 region identifier, e.g. <code>US</code>, or <code>HK</code>.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Classes

This module exposes no classes.

