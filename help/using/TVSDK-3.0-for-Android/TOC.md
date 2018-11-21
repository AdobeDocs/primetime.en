---
cloud: experience-cloud
product: adobe
archtype: end-user
user-guide: null
---

# Table of Contents {#table-of-contents}

+ Introduction {#introduction}
   + [Product overview, audience, and this guide](android-3.0-introduction/overview-prod-audience-guide/android-3.0-overview-prod-audience-guide.md)
   + [Considerations and best practices](android-3.0-introduction/overview-prod-audience-guide/android-3.0-considerations.md)
   + [Primetime TVSDK features](android-3.0-introduction/overview-prod-audience-guide/android-3.0-overview-of-the-player.md)
   + [Requirements](android-3.0-introduction/android-3.0-requirements.md)
+ Content playback options {#content-playback-options}
   + [Set up the Media player](android-3.0-content-playback-options-android2/android-3.0-mediaplayer-set-up-android.md)
   + Work with MediaPlayer objects {#work-with-mediaplayer-objects}
      + [About the MediaPlayerItem class](android-3.0-content-playback-options-android2/mediaplayerobjects-working-with/android-3.0-mediaplayeritem-class-about.md)
      + [Lifecycle and statuses of the MediaPlayer object](android-3.0-content-playback-options-android2/mediaplayerobjects-working-with/android-3.0-mediaplayer-object-lifecycle-states.md)
      + [MediaPlayerItem methods for accessing MediaResource information](android-3.0-content-playback-options-android2/mediaplayerobjects-working-with/android-3.0-mediaplayeritem-accessing-mediaresource.md)
      + [Reuse or remove a MediaPlayer instance](android-3.0-content-playback-options-android2/mediaplayerobjects-working-with/android-3.0-mediaplayer-reuse-or-remove.md)
      + [Inspect the playback timeline](android-3.0-content-playback-options-android2/mediaplayerobjects-working-with/android-3.0-timeline-inspect-playback.md)
      + [Suspend and Restore MediaPlayer](android-3.0-content-playback-options-android2/mediaplayerobjects-working-with/android-3.0-suspend-and-restore.md)
   + Listen and implement Primetime Player events {#listen-and-implement-primetime-player-events}
	  + [Listen for Primetime Player events](android-3.0-content-playback-options-android2/events-listen-for/android-3.0-events-listen-for.md)
      + [Implement event listeners and callbacks](android-3.0-content-playback-options-android2/events-listen-for/android-3.0-event-listeners-implement.md)
   + [Set up error handling](android-3.0-content-playback-options-android2/android-3.0-error-handling-set-up.md)
   + Configure the player user interface {#configure-the-player-user-interface}
      + [Wait for a valid status](android-3.0-content-playback-options-android2/ui-configure/android-3.0-ui-state-prepared-wait-for.md)
      + [Play and pause a video](android-3.0-content-playback-options-android2/ui-configure/android-3.0-ui-pause-play-implement.md)
      + [Identify whether the content is live or VOD](android-3.0-content-playback-options-android2/ui-configure/android-3.0-ui-content-live-vod-identify.md)
      + [Provide volume control](android-3.0-content-playback-options-android2/ui-configure/android-3.0-ui-volume-control.md)
      + [No title available](android-3.0-content-playback-options-android2/ui-configure/t-psdk-android-3.0-ui-duration-time-display.md)
      + [Display a seek scrub bar with the current playback position](android-3.0-content-playback-options-android2/ui-configure/android-3.0-ui-seek-scrub-bar-display.md)
      + [Construct a control bar enhanced for DVR](android-3.0-content-playback-options-android2/ui-configure/android-3.0-ui-ctrl-bar-for-dvr-construct.md)
      + [Enter a stream at a specific time](android-3.0-content-playback-options-android2/ui-configure/android-3.0-ui-stream-entry-control.md)
   + Initialize the media player for a specific video {#initialize-the-media-player-for-a-specific-video}
      + [Create a media resource](android-3.0-content-playback-options-android2/mediaplayer-initialize-for-video/android-3.0-media-resource-create.md)
      + [Load a media resource in the media player](android-3.0-content-playback-options-android2/mediaplayer-initialize-for-video/android-3.0-media-resource-load.md)
      + [Load a media resource using MediaPlayerItemLoader](android-3.0-content-playback-options-android2/mediaplayer-initialize-for-video/android-3.0-media-resource-mediaplayeritemloader.md)
   + Implement fast forward and rewind {#implement-fast-forward-and-rewind}
	  + [Implement fast forward and rewind overview](android-3.0-content-playback-options-android2/trick-play-implement/android-3.0-trick-play-implement.md)
      + [Rate-change API elements](android-3.0-content-playback-options-android2/trick-play-implement/android-3.0-trick-play-apis.md)
      + [Limitations and behavior for trick play](android-3.0-content-playback-options-android2/trick-play-implement/android-3.0-trick-play-limitations.md)
      + [Smoother trick play operations](android-3.0-content-playback-options-android2/trick-play-implement/android-3.0-trick-play-smooth.md)
   + [HTTP 302 redirect optimization](android-3.0-content-playback-options-android2/android-3.0-302-redirect-overview.md)
   + [Work with cookies](android-3.0-content-playback-options-android2/android-3.0-cookies-work-with.md)
   + Work with closed captions {#work-with-closed-captions}
	  + [Work with closed captions overview](android-3.0-content-playback-options-android2/closed-captions-set-up/android-3.0-closed-captions-set-up.md)
      + [Select a current caption track from among available tracks](android-3.0-content-playback-options-android2/closed-captions-set-up/android-3.0-closed-caption-available.md)
      + [Control closed-caption visibility](android-3.0-content-playback-options-android2/closed-captions-set-up/closed-caption-visibility-control/android-3.0-closed-caption-visibility-control.md)
      + [Allow users to change the caption track](android-3.0-content-playback-options-android2/closed-captions-set-up/closed-caption-visibility-control/android-3.0-closed-caption-change.md)
      + [Control closed-caption styling](android-3.0-content-playback-options-android2/closed-captions-set-up/android-3.0-closed-caption-styling.md)
   + Alternate audio {#alternate-audio}
      + [Alternate audio overview](android-3.0-content-playback-options-android2/alternate-audio/android-3.0-alternate-audio.md)
      + [AC-3 5.1 format](android-3.0-content-playback-options-android2/alternate-audio/android-3.0-ac-3-5.1-format.md)
      + [Alternate audio tracks in the playlist](android-3.0-content-playback-options-android2/alternate-audio/android-3.0-alternate-audio-in-playlist.md)
      + [Access alternate audio tracks](android-3.0-content-playback-options-android2/alternate-audio/android-3.0-alternate-audio-implement.md)
   + [Enable background audio](android-3.0-content-playback-options-android2/android-3.0-background-audio.md)
   + [ID3 tags](android-3.0-content-playback-options-android2/android-3.0-id3-metadata-retrieve.md)
   + Buffering {#buffering}
      + [Buffering overview](android-3.0-content-playback-options-android2/buffering-configuration/android-3.0-buffering-configuration.md)
      + [Instant On](android-3.0-content-playback-options-android2/buffering-configuration/android-3.0-instant-on.md)
   + [Parallel downloads](android-3.0-content-playback-options-android2/android-3.0-parallel-downloads.md)
   + Adaptive bit rates (ABR) for video quality {#adaptive-bit-rates-(abr)-for-video-quality}
      + [Adaptive bit rates (ABR) for video quality overview](android-3.0-content-playback-options-android2/abr-control-quality/android-3.0-abr-control-quality.md)
      + [Configure adaptive bit rates using ABRControlParameters](android-3.0-content-playback-options-android2/abr-control-quality/android-3.0-abr-set-using-abrparameters.md)
   + [Quality of service statistics](android-3.0-content-playback-options-android2/android-3.0-qos-statistics-monitor.md)
   + [Playback and failover](#playback-and-failover)
      + [Playback and failover overview](android-3.0-content-playback-options-android2/failover-for-playback/android-3.0-failover-for-playback.md)
      + [Media playback and failover](android-3.0-content-playback-options-android2/failover-for-playback/android-3.0-failover-media-playback.md)
      + [Advertising insertion and failover for VOD](android-3.0-content-playback-options-android2/failover-for-playback/android-3.0-failover-ad-insertion-for-vod.md)
+ Advertising {#advertising}
   + [Advertising requirements](android-3.0-advertising/ad-insertion/android-3.0-ad-insertion-TOC.md) 
   + Insert ads {#insert-ads}
      + [Insert ads overview](android-3.0-advertising/ad-insertion/ad-insertion-about/android-3.0-ad-insertion-about.md)
      + [Resolve and insert VOD ad](android-3.0-advertising/ad-insertion/ad-insertion-about/android-3.0-ad-resolving-client-vod.md)
      + [Resolve and insert Live/linear ad](android-3.0-advertising/ad-insertion/ad-insertion-about/android-3.0-ad-resolving-client-live-linear.md)
      + [Implement an early ad break return](android-3.0-advertising/ad-insertion/ad-insertion-about/android-3.0-early-ad-break-return.md)
      + [Track client ad](android-3.0-advertising/ad-insertion/ad-insertion-about/android-3.0-ad-tracking-client.md)
      + [Client error handling for broken VMAP](android-3.0-advertising/ad-insertion/ad-insertion-about/android-3.0-broken-vmap-error.md)
      + [Secure Ad loading over HTTPS](android-3.0-advertising/ad-insertion/ad-insertion-about/android-3.0-secure-ad-loading.md)
   + [Default and customized playback behavior with ads](android-3.0-advertising/ad-insertion/android-3.0-playback-post1.2.md)
   + Customize playback with ads {#customize-playback-with-ads}
      + [Customize playback with ads overview](android-3.0-advertising/ad-insertion/playback-customize/android-3.0-playback-customize.md)
      + [API elements for ad playback](android-3.0-advertising/ad-insertion/playback-customize/android-3.0-playback-ad-custom-elements.md)
      + [Use the default playback behavior](android-3.0-advertising/ad-insertion/playback-customize/android-3.0-playback-use-default.md)
      + [Customize playback with ads](android-3.0-advertising/ad-insertion/playback-customize/android-3.0-playback-customize.md)
      + [Skip ad breaks for a period of time](android-3.0-advertising/ad-insertion/playback-customize/android-3.0-playback-skip-breaks.md)
      + [Save the video position and resume later](android-3.0-advertising/ad-insertion/playback-customize/android-3.0-playback-save-position.md)
      + [Partial Ad break insertion](android-3.0-advertising/ad-insertion/playback-customize/android-3.0-partial-ad-break-insertion.md)
   + [Just-in-Time Ad Resolving]{#just-in-time-ad-resolving}
      + [Just-in-Time Ad Resolving overview](android-3.0-advertising/ad-insertion/c-lazy-ad-resolving/c-lazy-ad-resolving.md)
      + [Enable lazy ad resolving](android-3.0-advertising/ad-insertion/c-lazy-ad-resolving/t-enable-lazy-ad-resolving.md)
   + [Upgrading from 2.5.x Lazy Ad Resolving to 3.0.0 Lazy Ad Resolving   (API/Workflow changes):](android-3.0-advertising/ad-insertion/t-upgrade-to-3.0.md)
   + Ad insertion metadata {#ad-insertion-metadata}
      + [Ad insertion metadata overview](android-3.0-advertising/ad-insertion/ad-insertion-metadata/android-3.0-ad-insertion-metadata.md)
      + [Set up ad insertion metadata](android-3.0-advertising/ad-insertion/ad-insertion-metadata/android-3.0-ad-insertion-metadata-set-up.md)
      + [Enable ads in full-event replay](android-3.0-advertising/ad-insertion/ad-insertion-metadata/ad-full-event-replay/android-3.0-ad-full-event-replay.md)
      + [Ad signaling mode](android-3.0-advertising/ad-insertion/ad-insertion-metadata/ad-full-event-replay/android-3.0-ad-signaling-mode.md)
   + Companion banner ads {#companion-banner-ads}
      + [Companion banner ads overview](android-3.0-advertising/ad-insertion/comp-banner-ads/android-3.0-companion-banner-ads.md)
      + [Best practices for companion banner ads](android-3.0-advertising/ad-insertion/comp-banner-ads/android-3.0-banners-best-practices.md)
      + [Companion banner data](android-3.0-advertising/ad-insertion/comp-banner-ads/android-3.0-companion-banner-data.md)
      + [Display banner ads](android-3.0-advertising/ad-insertion/comp-banner-ads/android-3.0-companion-banner-ads-display.md)
   + Clickable ads (#clickable-ads)
      + [Clickable ads overview](android-3.0-advertising/ad-insertion/clickable-ads/android-3.0-clickable-ads.md)
      + [Respond to clicks on ads](android-3.0-advertising/ad-insertion/clickable-ads/android-3.0-respond-to-ad-clicks.md)
      + [Separate the clickable ad process](android-3.0-advertising/ad-insertion/clickable-ads/android-3.0-separate-clickable-ad-process.md)
      + [Pause and resume playback](android-3.0-advertising/ad-insertion/clickable-ads/android-3.0-pausing-resuming-playback.md)
   + Repackage incompatible ads using Adobe Creative Repackaging Service (CRS) {#repackage-incompatible-ads-using-adobe-creative-repackaging-service-(crs)}
      + [Repackage incompatible ads using Adobe Creative Repackaging Service (CRS) overview](android-3.0-advertising/ad-insertion/ad-transcoding/android-3.0-ad-transcoding.md)
      + [Enable CRS in TVSDK applications](android-3.0-advertising/ad-insertion/ad-transcoding/android-3.0-enable-crs.md)
   + Ad fallback for VAST and VMAP ads {#ad-fallback-for-vast-and-vmap-ads}
      + [Ad fallback for VAST and VMAP ads overview](android-3.0-advertising/ad-insertion/ad-fallback/android-3.0-ad-fallback.md)
      + [Define fallback ad behavior for VMAP inline ads](android-3.0-advertising/ad-insertion/ad-fallback/android-3.0-ad-fallback-set-up.md)
      + [Ad fallback behavior for VAST and VMAP](android-3.0-advertising/ad-insertion/ad-fallback/android-3.0-ad-fallback-behavior.md)
   + Custom tags {#custom-tags}
      + [Custom tags overview](android-3.0-advertising/ad-insertion/custom-tags-configure/android-3.0-custom-tags-configure.md)
      + [Example of a customized VOD asset](android-3.0-advertising/ad-insertion/custom-tags-configure/android-3.0-custom-tags-overview.md)
      + [Config class methods for tags](android-3.0-advertising/ad-insertion/custom-tags-configure/android-3.0-custom-tags-psdkconfig-methods.md)
      + [Timed metadata class](android-3.0-advertising/ad-insertion/custom-tags-configure/android-3.0-custom-tags-timedmetadata-class.md)
      + [Subscribe to custom tags](android-3.0-advertising/ad-insertion/custom-tags-configure/android-3.0-custom-tags-subscribe.md)
      + [Add listeners for timed metadata notifications](android-3.0-advertising/ad-insertion/custom-tags-configure/android-3.0-custom-tags-receive-notifications.md)
      + [Store timed metadata objects as they are dispatched](android-3.0-advertising/ad-insertion/custom-tags-configure/android-3.0-timed-metadata-store.md)
   + VPAID 2.0 ad support {#vpaid-2.0-ad-support}
      + [VPAID 2.0 ad support overview](android-3.0-advertising/ad-insertion/vpaid-2.0-ads/android-3.0-vpaid-2.0-ads.md)
      + [Implement VPAID 2.0 integration](android-3.0-advertising/ad-insertion/vpaid-2.0-ads/android-3.0-include-vpaid20-support.md)
   + [Ad measurements from Moat](android-3.0-advertising/ad-insertion/android-3.0-ad-measurements-from-moat.md)
   + Add custom ad markers {#add-custom-ad-markers}
      + [Add custom ad markers overview](android-3.0-advertising/ad-insertion/ad-markers-add-custom/android-3.0-ad-markers-add-custom.md)
      + [TimeRange class](android-3.0-advertising/ad-insertion/ad-markers-add-custom/android-3.0-timerange-class.md)
      + [MediaPlayer and MediaResource classes](android-3.0-advertising/ad-insertion/ad-markers-add-custom/android-3.0-mediaplayer-mediaresource-classes.md)
      + [ReplaceTimeRange class](android-3.0-advertising/ad-insertion/ad-markers-add-custom/android-3.0-replacetimerange-class.md)
      + [Place custom ad markers on the timeline](android-3.0-advertising/ad-insertion/ad-markers-add-custom/android-3.0-place-custom-ad-markers-on-timeline.md)
      + [Control playback behavior for seeking over custom ad markers](android-3.0-advertising/ad-insertion/ad-markers-add-custom/android-3.0-ad-markers-control-seek.md)
   + Customize opportunity generators and content resolvers {#customize-opportunity-generators-and-content-resolvers}
      + [Customize opportunity generators and content resolvers overview](android-3.0-advertising/ad-insertion/content-resolver/android-3.0-content-resolver.md)
      + [Opportunity generators and content resolvers](android-3.0-advertising/ad-insertion/content-resolver/android-3.0-content-resolver-about.md)
      + [Implement a custom opportunity generator](android-3.0-advertising/ad-insertion/content-resolver/android-3.0-opp-detector-impl-android.md)
      + [Implement a custom content resolver](android-3.0-advertising/ad-insertion/content-resolver/android-3.0-content-resolver-implement.md)
   + Delete and replace ads in VOD streams {#delete-and-replace-ads-in-vod-streams}
      + [Delete and replace ads in VOD streams overview](android-3.0-advertising/ad-insertion/delete-replace-content-vod/android-3.0-delete-replace-content-vod.md)
      + [Custom time range operations](android-3.0-advertising/ad-insertion/delete-replace-content-vod/custom-time-range-ops/android-3.0-custom-time-range-ops-android.md)
      + [Content resolvers for ad deletion / replacement](android-3.0-advertising/ad-insertion/delete-replace-content-vod/custom-time-range-ops/android-3.0-content-resolvers-for-ad-deletion.md)
      + [Effect on ad insertion and deletion from ad signaling mode and ad metadata combinations](android-3.0-advertising/ad-insertion/delete-replace-content-vod/c-psdk-android-3.0-signaling-mode-metadata-combos-android.md)
      + [Use cases to delete and replace ads](android-3.0-advertising/ad-insertion/delete-replace-content-vod/ad-delete-replace-use-cases/android-3.0-ad-delete-replace-use-cases.md)
      + [Mark ranges](android-3.0-advertising/ad-insertion/delete-replace-content-vod/ad-delete-replace-use-cases/android-3.0-mark-ranges-android.md)
      + [Replace time ranges with an ad](android-3.0-advertising/ad-insertion/delete-replace-content-vod/ad-delete-replace-use-cases/android-3.0-replace-ranges-with-aud-ad-android.md)
      + [Delete ranges](android-3.0-advertising/ad-insertion/delete-replace-content-vod/ad-delete-replace-use-cases/android-3.0-delete-ranges-with-aud-ad-android.md)
      + [Examples to delete and replace ads](android-3.0-advertising/ad-insertion/delete-replace-content-vod/android-3.0-ad-delete-replace-examples.md)
      + [Ad deletion and replacement error handling](android-3.0-advertising/ad-insertion/delete-replace-content-vod/ad-delete-replace-error-handling/android-3.0-ad-delete-replace-error-handling.md)
      + [Time range error examples](android-3.0-advertising/ad-insertion/delete-replace-content-vod/ad-delete-replace-error-handling/android-3.0-timerange-error-examples-dhls.md)
   + Update ad creative selection rules {#update-ad-creative-selection-rules}
      + [Update ad creative selection rules overview](android-3.0-advertising/ad-insertion/android-3.0-updating-rules/android-3.0-updating-rules.md)
      + [Priority rules](android-3.0-advertising/ad-insertion/android-3.0-updating-rules/android-3.0-priority-rule.md)
      + [Normalize rules](android-3.0-advertising/ad-insertion/android-3.0-updating-rules/android-3.0-normalize-rule.md)
      + [Sample creative selection rules](android-3.0-advertising/ad-insertion/android-3.0-updating-rules/android-3.0-sample-rule-files.md)
      + [Apply creative selection rules](android-3.0-advertising/ad-insertion/android-3.0-updating-rules/android-3.0-how-tvsdk-applies-csr.md)
+ Content protection {#content-protection}
   + [Widevine DRM](android-3.0-content-security/android-3.0-drm-widevine.md)
   + [Primetime DRM interface overview](android-3.0-content-security/android-3.0-drm-interface.md)
   + [DRM authentication before playback](android-3.0-content-security/android-3.0-drm-auth-before-playback.md)
   + [DRM authentication during playback](android-3.0-content-security/android-3.0-drm-auth-during-playback.md)
+ Video analytics {#video-analytics}
   + [Integrating TVSDK with Adobe Analytics](va-integration-overview/android-3.0-va-integration-overview/android-3.0-va-integration-overview.md)
   + [Initialize and configure video analytics](va-integration-overview/android-3.0-va-integration-overview/android-3.0-va-integrate-heartbeats.md)
   + [Implement custom metadata support](va-integration-overview/android-3.0-va-integration-overview/android-3.0-va-custom-metadata.md)
   + [Implement chapter support](va-integration-overview/android-3.0-va-integration-overview/android-3.0-va-chapter-support.md)
   + [Set up video analytics reporting on the server side](va-integration-overview/android-3.0-va-integration-overview/android-3.0-va-server-side-reporting-set-up.md)
   + [Access video analytics reports](va-integration-overview/android-3.0-va-integration-overview/android-3.0-va-reports-access.md)
+ Events and notifications {#events-and-notifications}
   + [Notifications and events for player status, activity, errors, and logging](android-3.0-events-notifications/android-3.0-notification-system.md)
   + [Notification codes](android-3.0-events-notifications/notification-codes/android-3.0-notification-codes.md)
   + [Details for the NATIVE_ERROR notification](android-3.0-events-notifications/notification-codes/android-3.0-native-error-summary.md)
   + [Primetime player events summary](android-3.0-events-notifications/events-summary/android-3.0-events-summary.md)
   + [Events](android-3.0-events-notifications/events-summary/android-3.0-events.md)
+ Billing {#billing}
   + [Billing metrics](android-3.0-billing-title/billing/android-3.0-billing.md)
   + [Configure billing metrics](android-3.0-billing-title/billing/android-3.0-billing-config.md)
   + [Transmit billing metrics](android-3.0-billing-title/billing/android-3.0-billing-data-format.md)