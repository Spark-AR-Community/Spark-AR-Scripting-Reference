# StorageScope

The `StorageScope` class encapsulates different methods of storage for persistent objects.

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
      <td style="text-align:left"><code>get</code>
      </td>
      <td style="text-align:left">
        <p><code>get(key: String): Promise&lt;Object&gt;</code>
        </p>
        <p>Gets the value with the specified key Returns a <code>JS Promise</code> which
          will be fulfilled with a JavaScript object or an error.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>remove</code>
      </td>
      <td style="text-align:left">
        <p><code>remove(key: String): Promise&lt;&gt;</code>
        </p>
        <p>Removes the key. Returns a <code>JS Promise</code> or an error.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>set</code>
      </td>
      <td style="text-align:left"><code>set(key: String, value: Object): Promise&lt;&gt;</code> Sets the
        value for the key Returns a <code>JS Promise</code> or an error.</td>
    </tr>
  </tbody>
</table>