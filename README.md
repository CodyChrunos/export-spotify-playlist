# export-spotify-playlist
Export Spotify Playlist to Google Sheet and convert to YouTube.

Sure, here's a description of the provided Google Apps Script for exporting tracks from a Spotify playlist to a Google Sheet:

**Description:**

This Google Apps Script is designed to interact with the Spotify API and Google Sheets to retrieve and store information about tracks from a Spotify playlist. The script allows you to export the playlist's tracks, including their titles, artists, albums, and Spotify URLs, into a Google Sheet. Additionally, it features pagination to handle playlists with more than 100 tracks and ensures that the Google Sheet headers are added only if a specific cell (A3) is empty.

**Quick Setup:**

- Get the Google Sheet I made from [here](https://chrunos.com/export-spotify-playlist/#export+spotify+playlist+to+google+sheet) and make a copy of it.
- In your copy of the sheet, delete everything.
- Input the Spotify Playlist URL in A2.
- Click on “Custom Menu” and select “Get Playlist Tracks”.

**Manual Setup:**

1. **Set Up the Google Sheet:**
   - Create a Google Sheet or open an existing one.
   - In cell A2, paste the Spotify playlist URL from which you want to export tracks.
   - Optionally, you can leave cell A3 empty if you want the script to add headers to the Google Sheet.

2. **Copy and Deploy the Script:**
   - Go to `Extensions` -> `Apps Script` in your Google Sheet.
   - Delete any existing code in the script editor.
   - Copy and paste the provided script into the script editor.

3. **Set Up Spotify API Credentials:**
   - Obtain a Spotify API client ID and client secret from the [Spotify Developer Dashboard](https://developer.spotify.com/).
   - Replace the `clientId` and `clientSecret` in the script with your own credentials.
   - In the script, the `refreshToken` should be your Spotify refresh token. You can obtain it through Spotify's authentication process.

4. **Run the Script:**
   - Save the script in the Apps Script editor.
   - Run the `getPlaylistTracks()` function by clicking the play button or through a trigger.

5. **Exported Data:**
   - The script will retrieve and append information about the playlist's tracks in the Google Sheet, starting from the second row. The columns will be: Title, Artist, Album, and URL.

6. **Handling Large Playlists:**
   - The script has built-in pagination support, ensuring that all tracks are fetched from the Spotify playlist, even if it contains more than 100 tracks.

7. **Generate Headers (Optional):**
   - The script will generate headers in the Google Sheet only if cell A3 is left empty. If you prefer to manage headers manually, simply fill in cell A3 with your desired header text.

This script provides a convenient way to export Spotify playlist information to a Google Sheet for various purposes, including analysis, sharing, and more.

