# CUSTOMIZE GUIDE

このテンプレートは、A-Frame + MindAR の画像トラッキングを最小構成でカスタマイズするための土台です。

## 1. 差し替えるファイル

- `assets/targets.mind`
  - MindAR のコンパイル済みターゲットデータ
- `assets/model/scene.gltf`
  - 表示する 3D モデル

## 2. targets.mind の作成

1. `target-image.png` などの認識させたい画像を準備
2. MindAR Compiler で `.mind` を生成
3. 生成されたファイルを `assets/targets.mind` に配置

## 3. 3D モデルの差し替え

1. glTF/GLB 形式のモデルを準備
2. `assets/model/scene.gltf`（必要ならテクスチャ類も同階層）として配置
3. 表示サイズが大きすぎる/小さすぎる場合は、`index.html` の `scale` を調整

## 4. index.html の主要調整ポイント

- `mindar-image` の `imageTargetSrc`
- `mindar-image-target` の `targetIndex`
- `<a-gltf-model>` の `position` / `rotation` / `scale`

## 5. トラブルシューティング

- 認識しない場合
  - ターゲット画像の特徴点が少ない可能性があります
  - 印刷時にぼやけていないか確認してください
- モデルが表示されない場合
  - パスが正しいか、関連テクスチャが揃っているか確認してください
