# LiveStreamingComments

The `LiveStreamingComments` class provides access to the Facebook Live comments stream.

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
      <td style="text-align:left"><code>stream</code>
      </td>
      <td style="text-align:left">
        <p><code>(get) stream: EventSource (set) (Not Available)</code>
        </p>
        <p>Specifies an <code>EventSource</code> that emits an update every time the
          Live stream receives a new comment. You may <code>subscribe()</code> to the <code>EventSource</code> and
          provide it with a callback that takes a single argument; when the callback
          is called, this argument will have the properties <code>body</code> (containing
          the text of the comment), and <code>timestampInVideoMs</code> (containing
          the video timestamp in milliseconds at which the comment was submitted).
          The stream will only return comments that are displayed on the broadcaster&apos;s
          screen, which in the case of high comment volume will not include every
          comments. To process potentially large volumes of comments, use the Counter
          and Vote methods below.</p>
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
      <td style="text-align:left"><code>startHashtagCounter</code>
      </td>
      <td style="text-align:left">
        <p><code>startHashtagCounter(): EventSource</code>
        </p>
        <p>Returns an <code>EventSource</code> that emits an update every time there
          is a change in the count of comments on the Live stream that contain hashtags.
          Hashtags are counted in case insensitive mode. You may <code>subscribe()</code> to
          the <code>EventSource</code> and provide a callback that receives a single
          argument, which will be a JavaScript Object containing hashtagged strings
          to comment counts. The hashtags will be provided in a canonical format,
          which will generally be CamelCase (for example #FacebookLive or #GrilledCheese).
          Internally, only the first 500 hashtags will be tracked and only the top
          20 will be surfaced to the subscription. A maximum of 10 counter/vote subscriptions
          may be active at a time. If one is created beyond that limit then the oldest
          one will not receive any more updates. The subscription will receive a
          maximum of one update per second.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>startHashtagVote</code>
      </td>
      <td style="text-align:left">
        <p><code>startHashtagVote(): EventSource</code>
        </p>
        <p>This method is identical to <code>startHashtagCounter()</code> except that
          for each user only the first hashtag appeared in his/her comments will
          be counted.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>startMatchCounter</code>
      </td>
      <td style="text-align:left">
        <p><code>startMatchCounter(matchStrings, isCaseSensitive): EventSource</code>
        </p>
        <p>Returns an <code>EventSource</code> that emits an update every time there
          is a change in the count of comments on the Live stream that match one
          or more target strings. The <code>matchStrings</code> argument is an array
          of strings to search for in comments. The <code>isCaseSensitive</code> determines
          whether the string matching respects letter case. You may <code>subscribe()</code> to
          the <code>EventSource</code> and provide a callback that receives a single
          argument, which will be a JavaScript Object containing matched strings
          to comment counts. Up to 20 match strings may be requested in one counter.
          A maximum of 10 counter/vote subscriptions may be active at a time. If
          one is created beyond that limit then the oldest one will not receive any
          more updates. The subscription will receive a maximum of one update per
          second.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>startMatchVote</code>
      </td>
      <td style="text-align:left">
        <p><code>startMatchVote(matchStrings, isCaseSensitive): EventSource</code>
        </p>
        <p>This method is identical to <code>startMatchCounter()</code> except that
          for each user only the first matched string appearing in the comment will
          be counted.</p>
      </td>
    </tr>
  </tbody>
</table>