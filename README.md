# Custom Google Calendar Viewer

Google Calendar を **FullCalendar + Google Calendar API** で表示する  
**個人利用・限定公開向けの高カスタマイズカレンダーUI**。

---

## 概要

このプロジェクトは、Google公式の埋め込みカレンダーでは難しい  
**「表示制御・配色・情報量の調整」**を目的として作られています。

主に以下を実現しています：

- 複数カレンダーの同時表示
- カレンダーごとの表示 / 非表示切り替え
- タイトル・時間の表示 / 非表示制御
- タイトル非表示時のラベル表示（例：「予定あり」）
- 背景2色を曜日ごとに交互表示（縦罫線なしでも判別可能）
- ダークテーマ前提の配色設計
- ウィンドウが縦に短くなっても自然に縮むレイアウト
- 予定クリック時は「拡大表示」のみ（Google詳細ページへは遷移しない）

---

## 技術構成

- HTML / CSS / JavaScript（ビルド不要）
- [FullCalendar v6.x](https://fullcalendar.io/)
- Google Calendar API（APIキー方式）

---

## セットアップ

### 1. Google Calendar API キーの準備

1. Google Cloud Console でプロジェクトを作成
2. **Google Calendar API** を有効化
3. APIキーを作成
4. HTML 内の以下に設定

```js
const GOOGLE_API_KEY = "YOUR_API_KEY_HERE";
