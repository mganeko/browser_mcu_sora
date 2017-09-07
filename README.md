# Browser MCU Sora 

* Video/Audio mixing sample for [WebRTC SFU Sora](https://sora.shiguredo.jp/), using [Browser MCU Core](https://github.com/mganeko/browser_mcu_core) library
* Using [sora-js-sdk](https://github.com/shiguredo/sora-js-sdk)
* --
* [Browser MCU Core](https://github.com/mganeko/browser_mcu_core) ライブラリを利用した、[WebRTC SFU Sora](https://sora.shiguredo.jp/)向けの映像/音声合成サンプルです
* [sora-js-sdk](https://github.com/shiguredo/sora-js-sdk) をコピーして利用しています

## Confirmed Environment / 動作確認環境

* Chrome  58.0.3029.110 (64-bit) for MacOS X
* Firefox 54.04 (64-bit) for MacOS X

## Preparation / 準備

* NOTE: You need Sora server to try /  試すにはSoraサーバーが必要です

#### Install / インストール

```
git clone --recursive https://github.com/mganeko/browser_mcu_sora.git
```

setup in your own web server / Webサーバー上に配置してください

#### Try on GitHub pages / GitHub pages で試す

* try GitHub pages / GitHub pages で試す
  * https://mganeko.github.io/browser_mcu_sora/mcu.html


## How to Use / 使い方

* Prepare
  * Setup Sora server before using the sample
  * Connect to same channel_id from multiple browsers with multistream mode
* Open sora_mcu.html with Chrome/Firefox
* Specify Sora signaling URL to [Sora Server:], such as ws://myserver.com:3000/signaling
* Click [Initialize Sora Client] Button
* Specify the channel_id which connected with multistream above to [Channel ID:]
* Click [Connect] Button
* Then, videos/audios are mixed
* Specify another channel to [Mix Channel ID:] and click [Connect Mix] button, to publish mixed video/audio

--

* 事前準備
  * サンプル利用にはSoraサーバーが必要です
  * Soraサーバーの特定のチャネルIDに、multistreamモードで複数のブラウザで接続しておきます
* Chrome/Firefoxブラウザで sora_mcu.html を開きます
* [Sora Server:] にSoraサーバーのシグナリンングURLを入力します(ws://myserver.com:3000/signaling など)
* [Initialize Sora Client]ボタンを押します
* [Channel ID:]に、multisteramで接続しているチャネルIDを指定します
* [Connect]ボタンを押します
* 映像/音声が合成されます
* [Mix Channel ID:]を指定して[Connect Mix]ボタンを押すと、合成した映像/音声を指定したチャネルIDに配信することができます

#### NOTE / 注意

* mixed video will not be updated when window/tab is hidden
  * In headless browser, this is not a restriction
* mixのウィンドウ/タブが完全に隠れていると、合成した映像が更新されません
  * ヘッドレスブラウザの場合は、画面が見えなくても問題ありません


## License / ライセンス

* Browser MCU Sora is under the MIT license
* Using [sora.js](https://github.com/shiguredo/sora-js-sdk) under Apache License 2.0 
* Browser MCU Sora はMITランセンスで提供されます
* [sora.js](https://github.com/shiguredo/sora-js-sdk) は Apache License 2.0 で提供されているものを利用しています



