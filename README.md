# OC_neural-style

オープンキャンパスで作成した機械学習を用いたWebサービスです．
主な機能は、Webカメラで撮った写真を指定したスタイルに変換する機能です．
カメラで写真を連続撮影し，指定のスタイルに画像を変換するWebアプリです．[元となるプログラム](https://github.com/lengstrom/fast-style-transfer)

## 使い方
1. Web&アプリケーションサーバとなるPC上でイメージを作るために`docker build ./ -t fast-ns`を実行．
2. イメージをコンテナとして動かすために`nvidia-docker run --rm -e NVIDIA_VISIBLE_DEVICES=’0’ -p 5000:5000 -v $(pwd):/app fast-ns`を実行．
3. 閲覧用PCのブラウザから`(サーバPCのIPアドレス):5000`にアクセス．
imagesファルダのstyleに元となる画像があるので結果と見比べて見てください．
