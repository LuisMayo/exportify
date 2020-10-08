<a href="https://luismayo.github.io/spotify-ultrastar-downloader/exportify.html"><img src="screenshot.png"/></a>

Export your Spotify playlists to use them with the [node.js downloader script](https://github.com/LuisMayo/ultrastar-downloader) in order to be able to sing your favourite songs in ultrastar:

[https://luismayo.github.io/spotify-ultrastar-downloader/exportify.html](https://luismayo.github.io/spotify-ultrastar-downloader/exportify.html)

If you want to back-up your spotify playlists instead you may check the [exportify original project](https://github.com/watsonbox/exportify)

No data will be saved - the entire application runs in the browser.


## Usage

Click 'Get Started', grant Exportify read-only access to your playlists, then click the 'Export' button to export a playlist.

### Export Format

Track data is exported in [JSON](https://en.wikipedia.org/wiki/JSON) format with the following fields:

```typescript
export interface Petition {
    songs: Song[],
    username: string;
    password: string;
}

export interface Song {
    title: string;
    artist: string;
}
```


## Development

Developers wishing to make changes to Exportify should use a local web server. For example, using Node (in the Exportify repo dir):

```bash
npx http-server -c-1
```

Then open [http://localhost:8080/exportify.html](http://localhost:8080/exportify.html).


## Notes

- The export uses the HTML5 download attribute which is not [supported](http://caniuse.com/#feat=download) in all browsers. Where not supported the CSV will be rendered in the browser and must be saved manually.

- According to Spotify [documentation](https://developer.spotify.com/web-api/working-with-playlists/), "Folders are not returned through the Web API at the moment, nor can be created using it".


## Contributing

Since this is a tiny project we don't have strict rules about contributions. Just open a Pull Request to fix any of the project issues or any improvement you have percieved on your own. Any contributions which improve or fix the project will be accepted as long as they don't deviate too much from the project objectives. If you have doubts about whether the PR would be accepted or not you can open an issue before coding to ask for my opinion
