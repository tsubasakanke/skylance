# SKYLANCE

ブラウザで遊べるアーケード空戦ゲーム。インストール不要、最大4人のマルチプレイ対応。

- 1人用ミッション / チュートリアル / 対戦（最大4人。個人戦バトルロイヤル or チーム戦2対2、3ラウンド制で2ラウンド先取）
- マルチプレイは PeerJS（WebRTC）による P2P 通信。最初に部屋に入った人がホストになり、ホストが抜けると残りのメンバーから自動で次のホストが選ばれる。
- 必要なのは `index.html` 1ファイルだけ（Three.js と PeerJS は CDN から読み込み）。

## GitHub Pages で公開する手順（ブラウザだけでできる）

1. https://github.com にログイン（アカウントがなければ無料で作る）
2. 右上の「＋」→「New repository」
   - Repository name: `skylance`
   - **Public** を選ぶ（無料プランの GitHub Pages は Public リポジトリが必要）
   - 「Create repository」
3. 作ったリポジトリのページで「uploading an existing file」をクリック
   - この `index.html` をドラッグ＆ドロップ（README.md も一緒にどうぞ）
   - 下の「Commit changes」を押す
4. リポジトリの「Settings」→ 左メニュー「Pages」
   - Source: **Deploy from a branch**
   - Branch: **main** / **/(root)** →「Save」
5. 1〜2分待つと、同じ画面の上に URL が出る  
   `https://<あなたのユーザー名>.github.io/skylance/`
6. その URL を友達に送れば完成。全員「対戦」→ 同じ**ルームコード**を入れて「コードで参加」→ 待機室で全員「準備OK」でラウンド開始。

## 更新するとき

新しい `index.html` を、手順3と同じようにアップロードして上書き → Commit。1〜2分で反映される。

## つながらないとき

- 学校や会社の Wi-Fi は P2P 通信を制限していることがある。スマホのテザリングなど別の回線で試すと切り分けできる。
- Chrome / Edge / Safari の最新版を使う。
- ホストが抜けた直後は数秒間、相手が消えて再接続される（自動）。
