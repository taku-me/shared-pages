# shared-pages

人に見せるための静的ページの置き場(公開 repo)。GitHub Pages で `main` の直下をそのまま配る(ビルドは無い。`.nojekyll` で Jekyll の変換を止めている)。

- 配る先: https://taku-me.github.io/shared-pages/<フォルダ名>/
- 配り方の今の設定は `gh api repos/taku-me/shared-pages/pages` で見る(`source` が配る branch と場所、`status` が直近の build の状態)

## 置いてあるページ

- `scaj2026/`: SCAJ2026 の出展者一覧(AI が調査した情報を含む。誤りの可能性あり)

## ページの足し方

1. フォルダを 1 つ作り、`index.html` を置く(外部の読み込みの無い、そのフォルダで閉じたページにする)
2. PR を出す。必須チェック security-gate(`.github/workflows/security-gate.yml`、中身は fleet-skills)が通ることを確かめる
3. マージの後、`gh api repos/taku-me/shared-pages/pages/builds/latest -q .status` が `built` になれば配られている

公開 repo なので、秘密・個人の情報・社外に出せない資料を置かない。

## 改版履歴

- 2026-10-21 必須チェック security-gate の caller を置く(公開 repo 用) (#1)
- 2026-10-05 GitHub Pages で配る静的ページの置き場を作り、scaj2026 を置く (a9e3225)
