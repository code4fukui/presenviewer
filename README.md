# presenviewer

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A lightweight, browser-based presentation viewer that loads a presentation from a simple JSON configuration file and a series of numbered image slides.

## Live Demo

[**https://github.com/code4fukui/presenviewer](https://code4fukui.github.io/presenviewer/)

The demo link loads a default presentation. To view your own, see the usage instructions below.

### Samples

- [OSS x オープンデータ x こどもシビックテック](https://code4fukui.github.io/presenviewer/#https://taisukef.github.io/presen/opendata/20220323-OSSX-civictech/20220323-OSSX-civictech.json)
- [世界を変えよう福井から](https://code4fukui.github.io/presenviewer/#https://taisukef.github.io/presen/opendata/20220224-koshigaku/20220224-koshigaku.json)

## How to Use

To display your own presentation, you need a publicly accessible JSON file and a corresponding set of named image files.

### 1. Create a JSON Configuration File

Create a `.json` file that specifies the total number of pages (slides) in your presentation.

**Example: `my-presentation.json`**
```json
{
  "pages": 12
}
```

### 2. Prepare and Name Your Image Files

Your slide images must be in `.jpeg` format and named to correspond with the JSON file. The naming convention is to replace the `.json` extension with a zero-padded, 3-digit slide number.

- `my-presentation.json`
- `my-presentation.001.jpeg`
- `my-presentation.002.jpeg`
- `my-presentation.003.jpeg`
- ...and so on, up to the page count.

### 3. Construct the Viewer URL

Combine the viewer URL with the URL of your JSON file as a hash parameter.

**Format:**
```
https://code4fukui.github.io/presenviewer/#<URL_to_your_JSON_file>
```

**Example:**
```
https://code4fukui.github.io/presenviewer/#https://example.com/path/to/my-presentation.json
```

## Controls

Navigate the presentation using your mouse or keyboard.

- **Next Slide**: `→` (Right Arrow) or `Click`
- **Previous Slide**: `←` (Left Arrow)
- **First Slide**: `Home` or `Esc`
- **Last Slide**: `End`

## License

This project is licensed under the MIT License.