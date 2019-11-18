# google-voice-desktop
Google Voice Desktop App (made with Nativefier) with functional badge counter and new icon

Download the app from [Releases](https://github.com/taralika/google-voice-desktop/releases) section

Or you can build it yourself:
###### Pre-condition:
1. Install [Nativefier](https://github.com/jiahaog/nativefier/#installation)
2. Install [optional dependencies](https://github.com/jiahaog/nativefier/#optional-dependencies)
3. Install [librsvg](https://www.npmjs.com/package/librsvg)
###### Execute these commands:
```
wget https://upload.wikimedia.org/wikipedia/commons/7/78/Google_Voice_icon.svg
rsvg-convert -h 1000 -w 1000 Google_Voice_icon.svg > Google_Voice_icon.png
wget https://raw.githubusercontent.com/taralika/google-voice-desktop/master/counter.js
nativefier --name "Voice" --icon Google_Voice_icon.png --counter --bounce --inject counter.js "https://voice.google.com/"
```
