# InstructionModule

The `InstructionModule` class enables effects to provide instructions to the user.

## Example

```text
//==============================================================================
// The following example demonstrates how to hide an instruction when more than
// one face is detected and show it if not.
//
// Project setup:
// - Set the 'Max Faces' of the 'Face Tracking' capability to 2 or more
// - Add the 'Instructions' capability
// - Select 'Custom Instructions'
// - Add the 'Try it with friends' instruction
//==============================================================================

// Load in the required modules
const Instruction = require('Instruction');
const FaceTracking = require('FaceTracking');

// Define a boolean that will be true until 2 faces are detected
var show = FaceTracking.count.lt(2);

// Bind the visibility of the instruction to the boolean
Instruction.bind(show, 'try_with_friends');
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
      <td style="text-align:left"><code>automaticInstructionsEnabled</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) automaticInstructionsEnabled: boolean (set) (Not Available)</code>
        </p>
        <p>Specifies whether or not automatic instructions are enabled.</p>
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
      <td style="text-align:left"><code>bind</code>
      </td>
      <td style="text-align:left">
        <p><code>bind(enabled: BooleanSignal, token: StringSignal): void</code>
        </p>
        <p>When enabled, shows instruction for given token (you can find and select
          custom instruction tokens in project capabilities)</p>
        <p>To hide instruction simply set enabled to <code>false</code>.</p>
        <p>You can have at most one binding for instructions, meaning that setting
          a different binding would replace any previously created and setup binding
          for instructions.</p>
      </td>
    </tr>
  </tbody>
</table>## Classes

This module exposes no classes.

