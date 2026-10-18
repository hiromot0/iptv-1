# Organized personal test playlists

Chinese, Japanese and English entries from the public iptv-org language
playlists, linked to real XMLTV schedules. Korean channels are excluded.
All changes are isolated on `codex/personal-epg`.

## Direct import

| Resource | URL |
| --- | --- |
| Combined playlist with EPG | https://raw.githubusercontent.com/hiromot0/iptv-1/codex/personal-epg/personal/index.m3u |
| Chinese with EPG | https://raw.githubusercontent.com/hiromot0/iptv-1/codex/personal-epg/personal/zh.m3u |
| Japanese with EPG | https://raw.githubusercontent.com/hiromot0/iptv-1/codex/personal-epg/personal/ja.m3u |
| English with EPG | https://raw.githubusercontent.com/hiromot0/iptv-1/codex/personal-epg/personal/en.m3u |
| XMLTV | https://raw.githubusercontent.com/hiromot0/epg/codex/personal-epg/personal/guide.xml |

Add a playlist as a Link source in iTV. If necessary, paste the XMLTV URL in
Programme Guide settings and tap Load/Update Guide. The M3U headers already
advertise the guide with `url-tvg` and `x-tvg-url`.

## Organization

- `index.m3u`, `zh.m3u`, `ja.m3u`, `en.m3u`: only entries whose exact `tvg-id`
  has a verified current/future programme in the generated XMLTV snapshot.
- `all.m3u`, `all-zh.m3u`, `all-ja.m3u`, `all-en.m3u`: the complete corresponding
  language lists, including entries without a supported EPG source.
- `coverage.json`: generation time, upstream hashes, supported/missing channel
  IDs and schedule expiry times.

Entries are sorted by channel ID and stream URL, with identical ID/URL pairs
removed. Group names are prefixed with the language. Original stream addresses,
exact feed IDs, logos and per-stream options such as referrers/user agents are
preserved. There is no automatic HD/SD or regional feed merging. A loaded EPG
does not mean that a stream has passed playback testing.

The guide is a short-lived snapshot. See
[the EPG branch and refresh instructions](https://github.com/hiromot0/epg/tree/codex/personal-epg/personal).
No automatic refresh is enabled. This personal branch is separate from the
licensed synthetic iTV App Store review fixtures. Provider terms and geographic
availability still apply to linked streams and programme data.
