# Review notes - Live TV: M3U Player (com.m3uplay.livetv.player)

## URLs
- Marketing URL: https://build-data-solutions-sas.github.io/livetv-m3u-player/
- Support URL: https://build-data-solutions-sas.github.io/livetv-m3u-player/
- Privacy Policy: https://build-data-solutions-sas.github.io/livetv-m3u-player/privacy-policy/
- Terms of Use: https://build-data-solutions-sas.github.io/livetv-m3u-player/terms-of-use/
- Contact: chandlerpiper499410@gmail.com (developer: BUILD DATA SOLUTIONS SAS)

## Notes for the reviewer (paste into Play Console)
**Positioning.** Live TV: M3U Player is a media player for people who already have their own M3U / M3U8 playlists (from an IPTV provider, a public playlist, or a personal file) and want a clean Android app to organise and play them. It is a tool, like a file or video player. Dark, media-first design, no account, no login, no in-app purchases.

**Content policy.** The app contains NO channels, streams, playlists or media. Everything is loaded by the user from their own source. The app does not host, distribute or link to copyrighted content, and does not recommend where to find it. The listing and the in-app "Important Notice" (shown before adding a source) state that the user is responsible for only using content they have the right to access. Provider presets are generic shortcuts to third-party public playlist sources that we do not operate or endorse. No content is uploaded or shared by the app, so there is no user-generated content hosted on a server.

**What is different from other M3U players.** Calm, hierarchical home (banner, source tabs All/URL/File, playlist sections), a friendly empty state that guides adding the first playlist, minimal player controls, favorites / recent history / search, multiple named playlists, and no sign-in wall.

**Permissions / data.** INTERNET and network state for streaming; POST_NOTIFICATIONS is requested at runtime and optional. No location, contacts, storage-wide, accessibility or other sensitive permissions. Ads (AdMob mediation) and analytics/attribution SDKs are disclosed in the Privacy Policy and Data Safety. Cleartext HTTP is allowed because many user-supplied IPTV streams are served over HTTP.

## How to test (no login needed)
1. Launch the app: Splash, Language, 4 onboarding pages, then Home.
2. Tap Add Playlist and read the Important Notice, then continue.
3. Choose the URL option, enter a name (any), and paste this public community playlist:
   `https://iptv-org.github.io/iptv/languages/eng.m3u`
   (alternative, larger list: `https://iptv-org.github.io/iptv/index.m3u`). This is a third-party public list used only for testing; availability of individual streams depends on their sources and some channels may be offline or geo-blocked.
4. Open the playlist, tap any channel to play (fullscreen, controls). Try the heart (favorite), the channel overflow menu (play / favorite / rename / delete / info), Search, Recent History and Settings (Language, Text size, About, Policy, Rate).
5. Optional: Add Playlist via Upload File / Load from Device with any local .m3u file, or choose a Provider preset.

Test account: none required. No in-app purchases.
