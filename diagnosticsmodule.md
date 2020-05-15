# DiagnosticsModule

The `DiagnosticsModule` class enables diagnostic logging.

## Example

```text
//==============================================================================
// The following example demonstrates how to log messages to the Console and
// watch signal values.
//==============================================================================

// Load in the required modules
const Diagnostics = require('Diagnostics');
const FaceTracking = require('FaceTracking');
const Scene = require('Scene');

// Log a message to the Console
Diagnostics.log('Console message logged from the script.');

// Watch a signal's value in the Console
Diagnostics.watch("Mouth Openness - ", FaceTracking.face(0).mouth.openness);
```

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
      <td style="text-align:left"><code>getModuleNames</code>
      </td>
      <td style="text-align:left">
        <p><code>getModuleNames(): Array&lt;string&gt;</code>
        </p>
        <p>Returns an array of names of all the scripting modules that can be loaded
          through a <code>require</code> call. Note: This set of modules is based on
          the list of enabled capabilities.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>getTypeDescriptions</code>
      </td>
      <td style="text-align:left">
        <p><code>getTypeDescriptions(): Array&lt;string&gt;</code>
        </p>
        <p>Finds the descriptions for each type in the effect.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>log</code>
      </td>
      <td style="text-align:left">
        <p><code>log(content: Object): void</code>
        </p>
        <p>Flattens content to a string and prints it to the debug console. Note:
          this function can be reassigned to any var (i.e. <code>foo.log = Diagnostics.log;</code>)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>watch</code>
      </td>
      <td style="text-align:left">
        <p><code>watch(tag: String, signal:BoolSignal): void watch(tag: String, signal:ScalarSignal): void watch(tag: String, signal:StringSignal): void</code>
        </p>
        <p>Adds the specified signal to the watch view in AR Studio with the specified
          tag.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

This module exposes no classes.

