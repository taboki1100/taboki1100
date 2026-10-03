## 作ったもの

### 道の駅訪問記録

https://michinoeki-log-ten.vercel.app

全国1,200以上の道の駅を地図と一覧から探し、訪問日・5段階評価・メモを記録できるWebアプリです。都道府県ごとの達成率、ほかのユーザーの評価や公開メモの閲覧、プロフィールの公開・非公開の切り替えに対応しています。

| 分野 | 採用技術 |
| --- | --- |
| フロントエンド | Next.js 16（App Router）/ React 19 / TypeScript / Tailwind CSS v4 |
| 地図 | Leaflet / 地理院タイル / Natural Earth |
| バックエンド | Supabase（PostgreSQL / Auth）。Row Level Security と列単位の権限で、他人の記録を書き換えられないことをDB側で保証 |
| 認証 | Google OAuth |
| データ | 国土交通省の道の駅一覧と国土数値情報を変換して取り込み（差分確認 → 1トランザクションで適用） |
| テスト | Vitest / Testing Library / pgTAP（RLSのテスト）/ Playwright（E2E、axe によるアクセシビリティ検査） |
| CI / ホスティング | GitHub Actions / Vercel |
