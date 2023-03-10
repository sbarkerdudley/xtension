# Xtension

An experiment with WebExtensions API.

## manifest.json

- `manifest.json` is the only required file in a browser extension.
- `"manifest_version"`, `"version"`, and `"name"` are the only mandatory keys.
- A list of valid keys can be found on [MDN](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json#list_of_manifest.json_keys).

Example:

```json
{
  "name": "MyExtension",
  "manifest_version": 3,
  "version": "1.0"
}
```

### `"manifest_version"`

- Acceptable values are an integer, either `2` or `3`.
- As of March 2023, version `2` is supported by all major browsers, but will soon be deprecated. Version `3` is not yet supported by Edge, nor Opera. - Version `1` is no longer supported.

A browser compatability chart from [MDN](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/manifest_version#browser_compatibility)


## Packaging the browser extension

Linux / macOS:
```sh
./bin/build.sh
```

_Create a zip file from the contents of `src/`, and save as a `.zip` file in the repository root directory._

- [`zip`](https://linux.die.net/man/1/zip) man page
- [Mozilla](https://extensionworkshop.com/documentation/publish/package-your-extension/) guide to packaging and publishing an extension
