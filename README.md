# PlayAdd for Spotify

PlayAdd for Spotify is a Google Chrome extension that makes it easier to add music being played on YouTube to your Spotify
playlists. This extension connects to your Spotify account and automatically detects when a song is being played on YouTube.
Upon clicking the extension icon in the browser bar, the song being played will be displayed with a link along with a list of your Spotify
playlists so you can quickly add the song to a playlist.

## Chrome Web Store

[Install](https://chrome.google.com/webstore/detail/playadd-for-spotify/ohnjhcegdijnbpbpgmmkdjmmeekomlfk) this extension directly from the Chrome Web Store. 

## Installing The Extension

For regular or development use, you can also choose to download this project and manually install it.

1. In Google Chrome, go to the extensions page by either navigating to chrome://extensions in the browser search bar or through the settings menu.
2. Enable the "Developer Mode" toggle button located on the extensions page.
3. Click on the "Load unpacked" button which should open a file browser window. Navigate to this project's root directory and select it.

# Local Development

For an entirely local installion and development, follow the instructions below. Running the server locally
is only required when wanting to make changes to the server.js file. **The following steps are not required when**
**making changes to any non-server.js file**.

## 1. Installation

1. Download Node.js
2. Navigate to the project directory in the console.
3. Run the following command to install all node modules.

```bash
npm install
```

## 2. .env

In order to store some sensitive information such as the Spotify Client ID and Client Secret loccally, you must create a .env file.
This file has no name, simply a .env file extension which should be created in the root directory of this project.
**DO NOT publish this file to a repository**. The file should contain the following.

```text
EXTENSION_DOMAIN = https://<extension_id>.chromiumapp.org
SPOTIFY_CLIENT_ID = <client_id>
SPOTIFY_CLIENT_SECRET = <client_secret>
SPOTIFY_REDIRECT_URL = http://localhost:3000
```

## 3. Starting The Server Locally

To start the server for local development, run the following command within the project directory.

```bash
npm start
```

The project uses nodemon, any changes made to server are automatically applied when the file is saved. Upon saving, the server stops, applies the changes, and restarts.
