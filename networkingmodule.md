# NetworkingModule

We’re temporarily disabling this capability while we work to improve performance and functionality. We'll reintroduce networking in the near future.

The `NetworkingModule` class enables effects to fetch information from a network. To use the Networking class you must add the Networking capability to the project manifest. You also need to whitelist domains you'd like to access in the Capabilities menu. AR Studio requires the URL passed to the `fetch()` method to be an HTTPS URL, with a certificate that chains up to a trusted certificate authority. Self-signed and other non-trusted certificates should not be expected to work.

## Example

```text
//==============================================================================
// The following example demonstrates how to send a JSON request to an online
// API.
//
// Project setup:
// - Whitelist the jsonplaceholder.typicode.com domain in Capabilities
//==============================================================================

// Load in the required modules
const Diagnostics = require('Diagnostics');
const Networking = require('Networking');

//==============================================================================
// Create the request
//==============================================================================

// Store the URL we're sending the request to
const url = 'https://jsonplaceholder.typicode.com/posts';

// Create a request object
const request = {

  // The HTTP Method of the request
  // (https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
  method: 'POST',

  // The HTTP Headers of the request
  // (https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
  headers: {'Content-type': 'application/json; charset=UTF-8'},

  // The data to send, in string format
  body: JSON.stringify({title: 'Networking Module'})

};

//==============================================================================
// Send the request and log the results
//==============================================================================

// Send the request to the url
Networking.fetch(url, request).then(function(result) {

  // Check the status of the result
  // (https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
  if ((result.status >= 200) && (result.status < 300)) {

    // If the request was successful, chain the JSON forward
    return result.json();

  }

  // If the request was not successful, throw an error
  throw new Error('HTTP status code - ' + result.status);

}).then(function(json) {

  // Log the JSON obtained by the successful request
  Diagnostics.log('Successfully sent - ' + json.title);

}).catch(function(error) {

  // Log any errors that may have happened with the request
  Diagnostics.log('Error - ' + error.message);

});
```

## Properties

This module exposes no properties.

## Methods

| Method | Description |
| :--- | :--- |
| `fetch` | `fetch(url: String) : Promise<ResponseObject>` Returns a promise for the result of the call. A `then()` clause attached to this takes a single argument; that argument is a callback function which takes a single argument, which is the result of the call. The result of the call is an object with two elements: A status property indicating the HTTP response status of the call, and `json()` function, which returns a promise for the dictionary containing the body of the response \(which is expected to be JSON\). |

## Classes

This module exposes no classes.

