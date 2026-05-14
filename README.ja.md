# presenviewer

シンプルなJSON設定ファイルと連番の画像スライドからプレゼンテーションを読み込む、軽量なブラウザベースのプレゼンビューアです。

## ライブデモ

[**https://github.com/code4fukui/presenviewer](https://code4fukui.github.io/presenviewer/)

このデモリンクはデフォルトのプレゼンテーションを読み込みます。独自のプレゼンテーションを表示するには、以下の使い方をご覧ください。

### サンプル

- [OSS x オープンデータ x こどもシビックテック](https://code4fukui.github.io/presenviewer/#https://taisukef.github.io/presen/opendata/20220323-OSSX-civictech/20220323-OSSX-civictech.json)
- [世界を変えよう福井から](https://code4fukui.github.io/presenviewer/#https://taisukef.github.io/presen/opendata/20220224-koshigaku/20220224-koshigaku.json)

## 使い方

独自のプレゼンテーションを表示するには、パブリックにアクセス可能なJSONファイルと、それに対応する名前の画像ファイル群が必要です。

### 1. JSON設定ファイルの作成

プレゼンテーションの総ページ数（スライド数）を指定する `.json` ファイルを作成します。

**例: `my-presentation.json`**
```json
{
  "pages": 12
}
```

### 2. 画像ファイルの準備と命名

スライド画像は `.jpeg` 形式とし、JSONファイルに対応した名前を付ける必要があります。命名規則として、拡張子 `.json` をゼロ埋めした3桁のスライド番号に置き換えます。

- `my-presentation.json`
- `my-presentation.001.jpeg`
- `my-presentation.002.jpeg`
- `my-presentation.003.jpeg`
- ...以降、ページ数に達するまで同様に続きます。

### 3. ビューアURLの構築

ビューアのURLと、JSONファイルのURLをハッシュパラメータとして結合します。

**形式:**
```
https://code4fukui.github.io/presenviewer/#<URL_to_your_JSON_file>
```

**例:**
```
https://code4fukui.github.io/presenviewer/#https://example.com/path/to/my-presentation.json
```

## 操作方法

マウスまたはキーボードでプレゼンテーションを操作できます。

- **次のスライド**: `→`（右矢印）または `クリック`
- **前のスライド**: `←`（左矢印）
- **最初のスライド**: `Home` または `Esc`
- **最後のスライド**: `End`

## ライセンス

このプロジェクトは MIT License のもとで公開されています。
