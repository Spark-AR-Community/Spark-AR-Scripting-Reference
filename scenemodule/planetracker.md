# PlaneTracker

The `PlaneTracker` class provides functionality for locating a 3D plane based on 2D screen coordinates.

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
      <td style="text-align:left"><code>confidence</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) confidence: StringSignal (set) (Not Available)</code>
        </p>
        <p>Returns tracking confidence level info. This value indicates if PlaneTracker
          is currently tracking and how confident it is in reported results. Possible
          values: - HIGH - MEDIUM - LOW - NOT_TRACKING</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>trackingMode</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) trackingMode: SceneModule.TrackingMode (set) trackingMode: SceneModule.TrackingMode</code>
        </p>
        <p>Specifies if this tracker object should track horizontal plane or moving
          object.</p>
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
      <td style="text-align:left"><code>hitTest</code>
      </td>
      <td style="text-align:left">
        <p><code>hitTest(screenLocation: Point2D): Point3D</code>
        </p>
        <p>Returns a point on tracked plane in local coordinates of PlaneTracker
          (in 3D units). Returns null if tracked plane is not found at given screen
          point.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>trackPoint</code>
      </td>
      <td style="text-align:left">
        <p><code>trackPoint(screenLocation: Point2D): void trackPoint(screenX: number, screenY: number): void trackPoint(screenLocation: PixelPointSignal, gestureState: StringSignal): void</code>
        </p>
        <p>PlaneTracker origin is bound to a point in 3d space, located on detected
          plane. This method updates PlaneTracker to track 3d point currently under
          given screen coordiantes. This also triggers new plane detection, in result
          this object&apos;s transform will be modified.</p>
        <p>Version with signal parameters can be used in touch gestures for continuous
          updating:</p>
        <p><code>TouchGestures.onPan().subscribe(function(gesture) { planeTracker.trackPoint(gesture.location, gesture.state); });</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>