---
layout: post
title:  "Exploring HTML5 Video and the Media API"
date:   2016-07-19 18:16:29 +1000
category: blog
description:
slug: exploring-html5-video-and-the-media-api
---

The `<video>` element was introduced in the HTML5 specification draft when it was released a few years ago, and a welcome addition it was indeed!

A highlight of the draft, the video element brought the web community a defined standard capable of showing accessible video content in the browser. We no longer need Flash!

The video element comes with all the features you need a video player to do:

- Controls for play, pause, volume, mute and fullscreen
- Declare a video in different formats in order to support a range of browsers
- Include transcripts used for closed captions
- Set an image to show when the video isn't playing, known as a poster

There can be a lot of fun had in working with video on the web and the video element. Combine this with some javascript from the Media API and you can create some solid video material for you websites.

<br>

## Basic code example

Below you can see a basic example of the video element, which includes displaying the controls, as well as fallback text with an explaination to users of browsers that don't support it.


    <div class="video-container">
        <video id="product-video" controls><source src="amazing-video.mp4" type="video/mp4"></source>
            Your browser does not support the <code>video</code> element.
        </video></div>

<br>

## Explanation of attributes used

The video element has a few attributes available for use. These are the more common ones.

Attribute     |  Description
------------- | -------------
`controls`    | set whether or not to show video controls
`poster`      | an image displayed when the video is not playing
`loop`        | a boolean value for setting the option to restart the video once it has finished playing
`src`         | the source file of the video <br>_Note: However you will find out below the use of_ `<source>` _inside_ `<video>` _provides better browser support coverage._

You can find more attributes for the video element at the [W3C wiki page](https://www.w3.org/wiki/HTML/Elements/video#HTML_Attributes).

<br>

## Media Events

There are a number of events being used to handle video content. Here are a few with a brief description.

### Playing
Sent when the media either begins to play or resume to play, after being paused or restarted if it has ended.

### Pause
The pause event is sent when playback is paused.

### Play
The play event is sent when playback starts after having been paused. A pause event must have been sent before the media can resume to play.

### Progress
The progress event is used to tell us how much of the media has been downloaded. This information is then made available in the media element's buffered attribute.

### Ended
Sent when media playback completes.

You can find a more detailed list of media events the [MDN Media Events page](https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Media_events).