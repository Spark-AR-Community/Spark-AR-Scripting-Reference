# CameraInfoModule

The `CameraInfoModule` class provides access to details about the device camera.

## Example

```text
//==============================================================================
// The following example demonstrates how to hide an object when capturing a
// photo or recording a video.
//
// Project setup:
// - Insert a plane
//==============================================================================

// Load in the required modules
const CameraInfo = require('CameraInfo');
const Scene = require('Scene');

// Locate the plane in the Scene
const plane = Scene.root.find('plane0');

//==============================================================================
// Hide the plane when capturing a photo or recording a video
//==============================================================================

// Store references to the photo capture and video recording boolean signals
const isCapturingPhoto = CameraInfo.isCapturingPhoto;
const isRecordingVideo = CameraInfo.isRecordingVideo;

// Create a boolean signal that returns true if either boolean signal are true
const hidePlane = isCapturingPhoto.or(isRecordingVideo);

// Bind the hidePlane signal to the hidden property of the plane
plane.hidden = hidePlane;
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
      <td style="text-align:left"><code>captureDevicePosition</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) captureDevicePosition: Signal&lt;CameraPosition&gt; (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>CameraPosition</code> enum signal identifying the current
          camera in use on the device.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>effectSafeAreaInsets</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) effectSafeAreaInsets: InsetsSignal (set) (Not Available)</code>
        </p>
        <p>Specifies an <code>InsetsSignal</code> indicating the insets of the effect
          safe area.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>isCapturingPhoto</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) isCapturingPhoto: BoolSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>BoolSignal</code> that indicates whether the camera is
          capturing a photo.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>isRecordingVideo</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) isRecordingVideo: BoolSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>BoolSignal</code> that indicates whether the camera is
          recording video.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>previewScreenScale</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) previewScreenScale: ScalarSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>ScalarSignal</code> describing the scale of the preview&apos;s
          screen, i.e. the number of pixels per point.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>previewSize</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) previewSize: PixelSizeSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>PixelSizeSignal</code> describing the size of the preview,
          in pixels.</p>
      </td>
    </tr>
  </tbody>
</table>## Methods

This module exposes no methods.

## Classes

This module exposes no classes.

## Enums

| Enum | Description |
| :--- | :--- |
| [`CameraPosition`](https://sparkar.facebook.com/docs/ar-studio/reference/enums/camerainfomodule.cameraposition) | The `CameraPosition` enum describes the direction the camera is facing. |

