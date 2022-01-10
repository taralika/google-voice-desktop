UPDATE: If you came here to get a desktop version of Google Voice, then you're in the right place except this app is no longer being maintained actively (it may still work, but YMMV). The good news is that you can now (at least as of v92 of Chrome) make any website act as an app directly through Chrome: In Chrome on your PC/Mac, open the website e.g., voice.google.com then go to the browser menu (3 dots in top right), choose "More Tools" > "Create Shortcut" - Make sure to select "Open as window" - and now you'll get Voice to open in its own window like an app. Pin the icon to your desktop/task/app bar for quick access. Detailed instructions here: you don't need my app anymore. Just go to voice.google.com in Chrome and you can create a shortcut/app that opens in its own window and you can pin its shortcut/icon to your dock just like any app. Detailed instructions are here: https://www.hellotech.com/guide/for/how-to-create-a-desktop-shortcut-to-a-website

# Google Voice Desktop
Google Voice Desktop App (made with Nativefier) with functional badge counter and new icon. The badge counter shows total of all unread items (texts, calls, voicemails). If new item arrives, badge counter will auto increment. As items are read, badge counter will automatically decrement. If you have desktop notifications turned on in your Google Voice account settings, the app will send notifications to desktop as new items arrive.

![icon-counter](/resources/google-voice-icon-readme.png)

## Download
[Latest release](https://github.com/taralika/google-voice-desktop/releases/latest)

## Build it yourself:
###### Pre-condition:
1. Install [Nativefier](https://github.com/jiahaog/nativefier/#installation)
2. Install [optional dependencies](https://github.com/jiahaog/nativefier/#optional-dependencies)
3. Install [librsvg](https://www.npmjs.com/package/librsvg)
###### Execute these commands:
```
wget https://upload.wikimedia.org/wikipedia/commons/7/78/Google_Voice_icon.svg
rsvg-convert -h 1000 -w 1000 Google_Voice_icon.svg > Google_Voice_icon.png
wget https://raw.githubusercontent.com/taralika/google-voice-desktop/master/counter.js
nativefier --name "Voice" --icon Google_Voice_icon.png --user-agent "Mozilla/5.0 (Windows NT 10.0; rv:99.0) Gecko/20100101 Firefox/99.0" --counter --inject counter.js "https://voice.google.com/"
```
