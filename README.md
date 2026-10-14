# Mikan Doodles 🍊✏️

**手描きみかん図鑑** — a tiny gallery site for hand-drawn mikan drawings.
Built for **Hack Club [Paperclip](https://paperclip.hackclub.com/)** ("Draw your own Assets, get Art Supplies!").

> ⚠️ すべての絵は**手描き**（紙に描いて撮影/スキャン、またはPCでマウス/ペンタブで描画）。AI生成アセットは不可。

## 現状

- サイトの骨組みは完成（`index.html` — ギャラリーグリッド、未描画スロットは自動でプレースホルダ表示）
- **描くのはユーザー本人** — 下の手順で絵を追加 → push すると即公開ページに反映

## 描くものリスト（6枚）

| # | ファイル名 | お題 |
|---|---|---|
| 1 | `assets/01-mikan-hello.png` | こんにちは — 基本ポーズ |
| 2 | `assets/02-mikan-sleep.png` | おひるね — まるくなる |
| 3 | `assets/03-mikan-run.png` | ダッシュ — 走る |
| 4 | `assets/04-mikan-friends.png` | なかまたち |
| 5 | `assets/05-mikan-focus.png` | 集中（みかんフォーカスより） |
| 6 | `assets/06-mikan-halloween.png` | ハロウィンみかん |

紙のサイズ・画材は自由（コピック、色鉛筆、ペン等）。正方形（1:1）がきれいに収まります。

## 手順（ユーザー向け）

1. **Lapseを開く**: https://lapse.hackclub.com → Create
   - 紙に描く場合 → **Camera モード**（Webcamで作業を録画）
   - PCで描く場合 → **Browser / Desktop モード**（画面を録画）
2. 描画セッションを録画しながら絵を描く（1枚ごと or まとめて）
3. 描き終わったら録画を保存 → **Lapseのリンクを控える**（提出に必要）
4. 絵をPNGに（紙なら撮影/スキャン、PCなら書き出し）→ ファイル名を上の表のとおりにして `assets/` に置く
5. `git add -A && git commit -m "add drawing #N" && git push` → 公開ページに反映

## 提出（Paperclip / 11/1 締切）

フォーム: https://forms.hackclub.com/paper-clip-submit

必要項目:
- Playable URL: https://maebahesioru.github.io/mikan-doodles/
- Code URL: https://github.com/maebahesioru/mikan-doodles
- Description: 手描きみかんの図鑑サイト（全アセット手描き）
- Screenshot: ギャラリーのスクショ
- **Hackatime Project Name(s): `mikan-doodles`**（下記で計測）
- **Lapse Link(s): Lapseの録画リンク**
- GitHub Username: maebahesioru / Slack: (要ログイン) / 住所: 登録済みのもの
- 景品: Card Grant (Global) を選択（日本OK）

## Hackatime計測（エージェント用）

実作業中に2分間隔で:

```bash
~/.wakatime/wakatime-cli --entity "$(pwd)/index.html" --project mikan-doodles \
  --write --category "ai coding" --sync-ai-disabled --time <epoch>
```

## 構成

- `index.html` — ギャラリー（依存ゼロ・単一ファイル）
- `assets/placeholder.svg` — 未描画スロットの仮画像（onerrorで自動表示）
