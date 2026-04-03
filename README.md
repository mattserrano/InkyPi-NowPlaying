# InkyPi-NowPlaying
An InkyPi plugin to display album art and song metadata.

## 🎵 Features

- Display current album art and ID3 tag metadata from Subsonic music streaming servers
- Supports plugin style settings to configure customizable text and backgrounds

## 📸 Screenshot

## 🛠️ Installation

Currently, Subsonic media servers are the only supported music provider.

1. Clone this plugin into your `InkyPi/src/plugins/` directory:
```
git clone https://github.com/mattserrano/InkyPi-NowPlaying /path/to/InkyPi/src/plugins/
```
2. Add `SUBSONIC_USER` and `SUBSONIC_PASS` to the InkyPi `.env` file (or via the API key manager)
3. Add your Subsonic server URL in the plugin settings
4. Configure optional style settings and refresh the eInk display

## 💡 How it Works

This InkyPi plugin retrieves now playing data from Subsonic servers and displays cover art and ID3 metadata on your Raspberry Pi's eInk display. It currently calls Subsonics' [getNowPlaying](https://docs.subsonic.org/pages/api.jsp#getNowPlaying) and [getCoverArt](https://docs.subsonic.org/pages/api.jsp#getCoverArt) REST APIs.

REST API authentication is implemented with computed md5(password + salt) hashed request parameters.