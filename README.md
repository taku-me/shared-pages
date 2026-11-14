# shared-pages

共有用の静的ページ置き場(コードは無く、HTML をそのまま置く)。

- `scaj2026/index.html`: SCAJ2026 出展者一覧(AI が調査した情報を含む。誤りの可能性あり)。`noindex` を付けてある
- `.nojekyll`: GitHub Pages で Jekyll の処理を通さないための印
- `.github/workflows/security-gate.yml`: PR の必須チェック(fleet-skills の security-gate を呼ぶ。変えない)。基準は `.security-gate-baseline.json`

## ページを足す

`<名前>/index.html` を置いて、この README の一覧に 1 行足す。確かめ方: ブラウザでファイルを開く。

## 改版履歴

- 2026-10-21 security-gate の caller を置く(公開 repo 用) (#1)
- 2026-10-05 SCAJ2026 出展者一覧を足す (a9e3225)
