# 室蘭テクノセンター AI研修 教材サイト 引き継ぎメモ（ChatGPT担当向け）

## 概要
- 研修名：AIなんでも勉強会（初級編）〜ChatGPTを実際に使ってみよう〜
- 開催：2026年12月4日（金）14:00〜17:00　室蘭テクノセンター
- 公開期間（表示上）：2026年12月4日〜2027年2月3日
- 方式：GitHub ＋ Azure Static Web Apps（前回ニセコ研修と同じ）
- 役割：ChatGPT＝入れ物（リポジトリ・SWA・デプロイ）／Copilot＝中身（HTML・教材）／中澤＝確認と最終判断

## このフォルダの中身（そのままリポジトリ直下に配置すれば動きます）
| パス | 内容 |
|---|---|
| index.html | 研修教材サイトのトップ（デモ・ハンズオン①②・困ったとき） |
| prompts.html | 明日から使えるChatGPTプロンプト集（99種類・検索・コピー機能） |
| files/demo/demo1_memo.jpg | デモ① 手書き会議メモ（架空） |
| files/demo/demo2_kyuka_guide.pdf | デモ② 架空の休暇制度ガイド（7ページ） |
| files/handson2/*.xlsx / *.txt | ハンズオン② テーマA〜Eの架空データ（Excel版・テキスト版） |
| images/ | デモ③ ポスター画像の置き場所（現在は空） |
| staticwebapp.config.json | noindexヘッダー、txtの文字コード指定 |
| robots.txt | 検索エンジンにクロールさせない設定 |

## 仕様メモ
- 外部ライブラリ・ビルド不要の静的HTML（CSS/JSはHTML内に記述）。
- ファイル名・パスはすべて半角英数字（URLでの文字化け防止）。
- コピーボタンは https 上で動作（SWAの既定URLでOK）。
- デモ③の画像は images/demo3_poster_1.png / _2.png / _3.png を置くと自動表示。無ければ枠ごと非表示。

## ChatGPT側にお願いしたいこと
1. GitHubリポジトリ作成 → このフォルダ一式をpush
2. Azure Static Web Apps（Freeプラン想定）作成・GitHub Actions連携
3. 公開URLの確認と、短縮URL・QRコードの作成（スライドNo.17・34に掲載予定）
4. 公開期間終了時の非公開化手順の用意（削除しない場合も表示は残す）

## 公開前チェック
- [ ] index.html / prompts.html がスマホ・PCで表示できる
- [ ] 各ダウンロードリンク（PDF・xlsx・txt）が開ける
- [ ] コピーボタンが動く
- [ ] 会場Wi-Fiでアクセスできる
