# Media

## YouTube
[Guide](https://docs.google.com/document/d/1SP3mo4c4aFclQSJG4ECrCIqbrytPNm_f2LgtULTY25Y/edit)

---

## ExoPlayer

### Resources
[Intro](https://developer.android.com/guide/topics/media/exoplayer)

#### Developer Guide

- [ExoPlayer Guide](https://google.github.io/ExoPlayer/guide.html)

- - [Shrinking ExoPlayer](https://google.github.io/ExoPlayer/shrinking.html)

- - [Battery Consumption](https://google.github.io/ExoPlayer/battery-consumption.html)

- ##### Extensions

- -  [github.com/google/ExoPlayer/extensions](https://github.com/google/ExoPlayer/tree/release-v2/extensions/)

- -  [ExoPlayer IMA extension](https://github.com/google/ExoPlayer/tree/release-v2/extensions/ima) (ads loader)

- [Releases](https://github.com/google/ExoPlayer/releases)

#### Samples

- [Codelab (Instant App, Lifecycle, Adaptive Streaming, etc...)](https://codelabs.developers.google.com/codelabs/exoplayer-intro/#0)
- - [Customizing the user interface](https://codelabs.developers.google.com/codelabs/exoplayer-intro/#6)
- - - [exo_playback_control_view.xml](https://raw.githubusercontent.com/google/ExoPlayer/release-v2/library/ui/src/main/res/layout/exo_playback_control_view.xml) (use exact name to override default layout)

- [github.com/google/ExoPlayer](https://github.com/google/ExoPlayer)

- [github.com/google/ExoPlayer/tree/io18](https://github.com/google/ExoPlayer/tree/io18)

#### YouTube

- [Building feature-rich media apps with ExoPlayer (Google I/O '18)](https://www.youtube.com/watch?v=svdq1BWl4r8)

#### Medium

- [google-exoplayer blog](https://medium.com/google-exoplayer)

- [ExoPlayer 2 - MediaSource composition (subtitle file, looping, sequencing...)](https://medium.com/google-exoplayer/exoplayer-2-x-mediasource-composition-6c285fcbca1f)

### Considerations

#### Streaming Media
- Firebase Storage (streaming audio/video): [Download Data via URL](https://firebase.google.com/docs/storage/android/download-files#download_data_via_url)

- Github Issue: [Stream media without downloading](https://github.com/google/ExoPlayer/issues/5028)

#### Keep Device Awake

- Documentation: [Manage device awake state](https://developer.android.com/training/scheduling/)

- - [Keep the device awake](https://developer.android.com/training/scheduling/wakelock)

- StackOverflow: [Fragments and Configuration Change](https://stackoverflow.com/a/53908821/2253682)