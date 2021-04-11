# Kodi-Playlist-Card

This card displays the playlist running on the kodi entity. The refresh is automatic based on events triggered by the entity. 

This card is intented to be an alternative to an iframe containing Chorus.


| Playlist Audio | Playlist Video
| ---- | ---- 
<img src="https://raw.githubusercontent.com/jtbgroup/kodi-playlist-card/master/assets/playlist_audio.png" alt="Palylist Audio" width="400"/> | <img src="https://raw.githubusercontent.com/jtbgroup/kodi-playlist-card/master/assets/playlist_video.png" alt="Palylist Video" width="400"/>

## Requirements

This card requires a specific sensor that gets the data from Kodi. The sensor is provided by the custom component [Kodi Media Sensors](https://github.com/jtbgroup/kodi-media-sensors). You need at least version 2.0.0 of this component to use the card.

## Features:

The card will let you track the playlist of kodi. 
You can perform some actions directly from the card like removing an item from the playlist or play a specific entry in the playlist.

## Installation:

1. Install the custom component [Kodi Media Sensors](https://github.com/jtbgroup/kodi-media-sensors).
2. Install the card using HACS
3. Reference the new resouce in lovelace

```
- url: hacsfiles/kodi-playlist-card/kodi-playlist-card.js
  type: Javascript module
```


## Card options:

| Name | Type | Default | Since | Description |
|------|------|---------|-------|-------------|
| type | string	| **required** | v1.0.0 | `custom:kodi-playlist-card` |
| entity | string | **required** | v1.0.0 |  `sensor.kodi_playlist` |
| title | string | optional | v1.0.0 | The title of the card |
| show_thumbnail | boolean | optional | v1.1.2 | Default = false. Set to true if you want to show the thumbnails coming from kodi. Attention you can get problems when mixing http and https content; if so, leave it to false. |

**No need to pass the entity of the Kodi player as it is embedded in the data of the sensor.**