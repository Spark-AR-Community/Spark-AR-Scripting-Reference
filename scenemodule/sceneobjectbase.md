# SceneObjectBase

The `SceneObjectBase` class describes a scene object.

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
      <td style="text-align:left"><code>boundingBoxVisible</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) boundingBoxVisible: BoolSignal (set) (Not Available)</code>
        </p>
        <p>Represents whether or not the bounding box for the object is visible.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>cameraVisibility</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) cameraVisibility: CameraVisibility (set) (Not Available)</code>
        </p>
        <p>Represents the <code>CameraVisibility</code> that contains a set of flags
          that specify the scene object (and its descendants) visibility depending
          on the active camera.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>hidden</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) hidden: BoolSignal (set) hidden: BoolSignal</code>
        </p>
        <p>Specifies whether the scene object and its descendants are hidden.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>identifier</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) identifier: string (set) (Not Available)</code>
        </p>
        <p>Specifies the scene object unique identifier. This value is specified
          internally in AR Studio.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>materialIdentifier</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) materialIdentifier: string (set) (Not Available)</code>
        </p>
        <p>Specifies the unique material identifier assigned to scene object. This
          value is specified internally in AR Studio.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>name</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) name: string (set) (Not Available)</code>
        </p>
        <p>Specifies the scene object name. This is the unique identifier of the
          object within the list of its siblings (immediate child objects of the
          same parent object).</p>
        <p><b>Note</b>: the object name is specified in AR Studio UI during design
          time.</p>
        <p><b>Note</b>: the object name must only be unique withing the list of direct
          siblings. There can be more than object with the same name in the scene
          as soon as they have different parents.</p>
        <p><b>See Also</b>: <code>SceneObjectBase.child</code>, <code>SceneObjectBase.find</code>, <code>SceneModule.root</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>outputVisibility</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) outputVisibility: OutputVisibility (set) (Not Available)</code>
        </p>
        <p>Represents the <code>OutputVisibility</code> that contains a set of flags
          that specify the scene object (and its descendants) visibility depending
          on the output.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>parentWorldTransform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) parentWorldTransform: TransformSignal (set) (Not Available)</code>
        </p>
        <p>Specifies a <code>TransformSignal</code> object describing the parent&apos;s
          transformation relative to world coordinate system.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>transform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) transform: Transform (set) transform: TransformSignal</code>
        </p>
        <p>Represents the object transformation, in object&apos;s local coordinate
          system.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>worldTransform</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) worldTransform: WorldTransform (set) worldTransform: TransformSignal</code>
        </p>
        <p>Specifies a <code>TransformSignal</code> object describing the object&apos;s
          transformation relative to world coordinate system. World transform in
          not yet supported for Canvas and Legacy canvas. Accessing this property
          from such objects or any of their children is not allowed.</p>
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
      <td style="text-align:left"><code>child</code>
      </td>
      <td style="text-align:left">
        <p><code>child(name: string): SceneObjectBase</code>
        </p>
        <p>Returns a child object by name. An exception is thrown if the object isn&apos;t
          found.</p>
        <p><b>See Also</b>: <code>SceneObjectBase.find</code>, <code>SceneModule.root</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>find</code>
      </td>
      <td style="text-align:left">
        <p><code>find(name: string): SceneObjectBase</code>
        </p>
        <p>Returns a descendant object by name. An exception is thrown if the object
          isn&apos;t found or if more than one is found.</p>
        <p><b>Note</b>: object D is considered to be a descendant of object P if
          either D is a child of P or if such an object C which is a child of P exists
          that D is a descendant of C.</p>
        <p><b>See Also</b>: <code>SceneObjectBase.child</code>, <code>SceneModule.root</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>findAll</code>
      </td>
      <td style="text-align:left">
        <p><code>findAll(name: string): Promise&lt;Array&lt;SceneObjectBase&gt;&gt; findAll(name: string, config:{ recursive: bool }): Promise&lt;Array&lt;SceneObjectBase&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the all of the scene objects with
          given name or empty array if none was found.</p>
        <p><code>recursive</code> param of <code>config</code> controls whenever the
          find should be performed recursively (<code>true</code> by default). Empty
          array is returned in no objects are found.</p>
        <p><b>See Also</b>: <code>SceneObjectBase.findFirst</code>, <code>SceneObjectBase.findByPath</code>, <code>SceneModule.root</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>findByPath</code>
      </td>
      <td style="text-align:left">
        <p><code>findByPath(pathQuery: string): Promise&lt;Array&lt;SceneObjectBase&gt;&gt; findByPath(pathQuery: string, config: {limit: number}): Promise&lt;Array&lt;SceneObjectBase&gt;&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the all occurances of scene objects
          matching the path query or empty array if none was found.</p>
        <p>Path query format: <code>*</code> matches any characters sequence. <code>*</code> as
          standalone component matches one level of the scene tree (i.e. any child) <code>**</code> as
          standalone component matches any level of scene tree (will result in recursive
          find) <code>/</code> is a path component separator <code>\</code> can be used
          to include in component name any of the control characters (including &apos;\&apos;
          itself)</p>
        <p>Examples: <code>findByPath(&quot;*&quot;)</code> will match all the direct
          children of the caller. <code>findByPath(&quot;*/A&quot;)</code> will match
          all grandchildren of the caller named A. <code>findByPath(&quot;**/A&quot;)</code> will
          match all descendants of the caller named A. <code>findByPath(&quot;A*&quot;)</code> will
          match all children of the caller which name is prefixed with &apos;A&apos;,
          like &apos;ABC&apos;. <code>findByPath(&quot;**/*A*&quot;)</code> will match
          all descendants of the caller which name contains &apos;A&apos;, like &apos;AX&apos;
          and &apos;XA&apos;. <code>findByPath(&quot;**/A&quot;, {limit: 10})</code> will
          match at most first 10 descendants of the caller named A. <code>findByPath(&quot;\\*&quot;)</code> will
          match all children of the caller named *. <code>findByPath(&quot;\\\\&quot;)</code> will
          match all children of the caller named .</p>
        <p><code>limit</code> parameter describes if <code>findByPath</code> should
          finish the search if it finds specified number of results (default is no
          limit). Non-positive values for limit are treated as unlimited.</p>
        <p><b>Note</b>: object D is considered to be a descendant of object P if
          either D is a child of P or if such an object C which is a child of P exists
          that D is a descendant of C.</p>
        <p><b>See Also</b>: <code>SceneObjectBase.findAll</code>, <code>SceneObjectBase.findFirst</code>, <code>SceneModule.root</code>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>findFirst</code>
      </td>
      <td style="text-align:left">
        <p><code>findFirst(name: string): Promise&lt;SceneObjectBase&gt; findFirst(name: string, config:{ recursive: bool }): Promise&lt;SceneObjectBase&gt;</code>
        </p>
        <p>Returns a promise that is resolved with the first occurance of scene object
          with given name or null if none was found. <code>recursive</code> param of <code>config</code> controls
          whenever the find should be performed recursively (<code>true</code> by
          default).</p>
        <p><b>See Also</b>: <code>SceneObjectBase.findAll</code>, <code>SceneObjectBase.findByPath</code>, <code>SceneModule.root</code>.</p>
      </td>
    </tr>
  </tbody>
</table>