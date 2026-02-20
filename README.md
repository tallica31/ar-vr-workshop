# AR/VR Workshop (A-Frame + MindAR)

スマートフォンで GitHub Pages を開き、カメラで **画像マーカー** または **顔** を認識して、3D オブジェクトを表示するためのハンズオン教材です。

## 構成

- `01-image-tracking/` : Part 1 画像トラッキング AR
- `02-face-tracking/` : Part 2 顔トラッキング AR
- `03-customize-template/` : Part 3 カスタマイズ用テンプレート
- `docs/` : 講義資料（PDF）

> 注意: `targets.mind` / `*.gltf` / `*.png` / `*.pdf` はバイナリファイルのため、この初期状態では未配置です。各ディレクトリ内の `.gitkeep` が配置場所の目印です。

## 使い方（ローカル確認）

1. このリポジトリを clone
2. ルートで静的サーバーを起動
   - 例: `python3 -m http.server 8000`
3. `http://<PCのIP>:8000/` をスマートフォンで開く
4. 各パートの `index.html` を開く

## GitHub Pages での公開

1. GitHub リポジトリの **Settings > Pages** を開く
2. Branch を `main`（または公開対象ブランチ）/ `/ (root)` に設定
3. 公開 URL (`https://<username>.github.io/<repo>/`) へスマホでアクセス

## ハンズオン内容

### Part 1: 画像トラッキング (`01-image-tracking/`)

- MindAR Image Tracking を利用
- `targets.mind` で定義されたターゲット画像を検出
- 検出時に 3D モデル (`scene.gltf`) を表示

### Part 2: 顔トラッキング (`02-face-tracking/`)

- MindAR Face Tracking を利用
- 顔アンカーにメガネモデル (`glasses.gltf`) とテクスチャ (`face-effect.png`) を重畳

### Part 3: カスタマイズ (`03-customize-template/`)

- 画像ターゲット・3D モデルを差し替えるためのテンプレート
- `CUSTOMIZE-GUIDE.md` に手順を記載

## 参考

- A-Frame: https://aframe.io/
- MindAR: https://hiukim.github.io/mind-ar-js-doc/
