# InkyPi-NowPlaying
An InkyPi plugin to display alhum cover art on Subsonic compatible media servers.

## 🎵 Features

- Display current album art and ID3 tag metadata from Subsonic music streaming servers
- Display audio file format and bitrate
- Supports plugin style settings to configure customizable text and backgrounds

## 📸 Screenshot

<img width="1001" height="467" alt="Screenshot 2026-04-05 at 12 17 16 PM" src="https://github.com/user-attachments/assets/02089d77-f576-4e36-a9b8-4813ebff6d71" />

<img width="1000" height="816" alt="Screenshot 2026-04-05 at 12 19 45 PM" src="https://github.com/user-attachments/assets/f18928a8-3825-4493-a670-269f565bb39f" />

## 🛠️ Installation

Currently, Subsonic media servers are the only supported music provider.

1. Use the inkypi plugin CLI to install this plugin:
```
inkypi plugin install now_playing https://github.com/mattserrano/InkyPi-NowPlaying
```
2. Add `SUBSONIC_USER` and `SUBSONIC_PASS` to the InkyPi `.env` file (or via the API key manager)
3. Add your Subsonic server URL in the plugin settings
4. Configure optional style settings and refresh the eInk display

## 💡 How it Works

This InkyPi plugin retrieves now playing data from Subsonic servers and displays cover art and ID3 metadata on your Raspberry Pi's eInk display. It currently calls Subsonics' [getNowPlaying](https://docs.subsonic.org/pages/api.jsp#getNowPlaying) and [getCoverArt](https://docs.subsonic.org/pages/api.jsp#getCoverArt) REST APIs.

REST API authentication is implemented with computed md5(password + salt) hashed request parameters.

## 📄 License

This project is licensed under the GPL 3.0 license - see the LICENSE file for details.
