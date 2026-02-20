# AR/VR Workshop (A-Frame + MindAR)

スマートフォンから GitHub Pages で開ける、AR/VR 技術の基礎理解向けハンズオン教材です。  
A-Frame と MindAR を使い、**画像トラッキング**と**顔トラッキング**の2パターンを体験できます。

## 構成

- `01-image-tracking/` : Part 1 画像トラッキングAR
- `02-face-tracking/` : Part 2 顔トラッキングAR
- `03-customize-template/` : Part 3 カスタマイズテンプレート
- `docs/` : 講義資料（PDF想定）

> [!NOTE]
> `.mind` / `.png` / `.gltf` / `.pdf` などのバイナリファイルは、このリポジトリ初期版では未追加です。  
> 後から各 `assets/` 配下や `docs/` 配下に配置してください。

## GitHub Pages での公開

公開後はトップページに Part 1 / Part 2 / Part 3 のリンクが表示されます。

1. このリポジトリを GitHub に push
2. リポジトリの **Settings > Pages** を開く
3. **Deploy from a branch** を選択
4. Branch を `main`（または利用ブランチ） / `/ (root)` に設定
5. 発行された URL をスマートフォンで開く

## ローカル確認

ブラウザのカメラ権限が必要です。HTTPS か localhost で動かしてください。

```bash
python3 -m http.server 8000
```

- トップページ: `http://localhost:8000/`
- Part 1: `http://localhost:8000/01-image-tracking/`
- Part 2: `http://localhost:8000/02-face-tracking/`
- Part 3: `http://localhost:8000/03-customize-template/`

## 使い方（概要）

### Part 1: 画像トラッキング

- `assets/targets.mind` にターゲット情報を配置
- `assets/target-image.png` を印刷/表示し、カメラでかざす
- マーカーが認識されると 3D オブジェクトを表示

### Part 2: 顔トラッキング

- フロントカメラを有効化
- 顔ランドマークに追従してオブジェクトを表示

### Part 3: カスタマイズ

- 自分の画像/モデルに差し替えてオリジナル AR を作成
- 詳細は `03-customize-template/CUSTOMIZE-GUIDE.md` を参照

## 参考リンク

- A-Frame: https://aframe.io/
- MindAR: https://github.com/hiukim/mind-ar-js
