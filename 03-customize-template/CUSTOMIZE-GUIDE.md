# Part 3 カスタマイズガイド

## 目的

`03-customize-template/` をコピーして、独自の AR コンテンツを作成します。

## 手順

1. `assets/targets.mind` を自分のターゲット画像から作成したファイルに置き換える
2. `assets/model/scene.gltf` を表示したい 3D モデルに置き換える
3. `index.html` の `position` / `rotation` / `scale` を調整する
4. スマートフォンで動作確認する

## `.mind` ファイル作成のヒント

- MindAR のコンパイラを使って、画像から `targets.mind` を生成します
- 特徴点が多く、コントラストが高い画像のほうが認識しやすくなります

## よくある調整ポイント

- モデルが大きすぎる: `scale` を小さくする
- モデルが沈む: `position` の Y を上げる
- 向きが合わない: `rotation` の Y を調整する
