# SLACSホームページ管理のマニュアル

## 概要

SLACSホームページは，[GitHub Pages](https://docs.github.com/ja/pages/getting-started-with-github-pages/about-github-pages)というGitHubの機能によりウェブページ生成されています．サイトジェネレーター部分には[Jekyll](https://jekyllrb.com/)を用いています．

ウェブページ管理者は，基本的には `slacs-web` リポジトリの `docs` ディレクトリ以下を書き換えることでウェブページを更新します．主要なファイルはマークダウン(`.md`ファイル)で作成されています．

Gitの使い方やマークダウンの編集方法が不明な場合は，適宜，ネットで調べるのをお勧めします．

## 参考情報

- [GitHub Pages について - GitHub Docs](https://docs.github.com/ja/pages/getting-started-with-github-pages/about-github-pages): GitHub Pagesの概要について．
- [Jekyll • Simple, blog-aware, static sites | Transform your plain text into static websites and blogs](https://jekyllrb.com/): ページ生成の細かい設定をする場合に必要となるドキュメント．
  - 使用しているページデザインのテーマ: [pages-themes/slate: Slate is a Jekyll theme for GitHub Pages](https://github.com/pages-themes/slate)
- [Daring Fireball: Markdown](https://daringfireball.net/projects/markdown/)

## slacs-web管理について

slacs-webのディレクトリ構造（抜粋）は以下の通り．

```
./
├── archive
│   └── SLACS.tgz （← SLACS 1995 〜 SLACS 2021 までのアーカイブ）
├── docs (← このディレクトリ以下のファイルがウェブページとして公開される対象 )
│   ├── 1995 (← SLACS 1995のアーカイブ )
│   ├── 1996 (← SLACS 1996のアーカイブ)
│   ├── 1997 (← SLACS 1997のアーカイブ )
  .
  .
（中略）
  .
  .
│   ├── assets
│   │   └── css
│   │       └── style.scss (← slacs-webのCSSファイル．デフォルトテンプレートからの差分を記述 )
│   ├── _config.yml （← slacs-webのjekyllの設定 ）
│   ├── history
│   │   ├── by-hayashi.html (← 旧SLACSホームページからある「SLACS という名前の由来」のhtmlファイル )
│   │   ├── index.md (← 新「SLACSの歩み」のmdファイル )
│   │   └── old-history.html (← 旧「SLACSの歩み」のmdファイル )
│   ├── index.md (← トップページのmdファイル )
│   ├── _layouts
│   │   └── default.html (← テンプレートファイル．slateテンプレートから取ってきたものを一部拡張 )
│   └── slacs-general.gif (← SLACSロゴの画像ファイル )
├── manual
│   ├── organize.md (← 各年度のSLACS幹事の引き継ぎマニュアル )
│   └── webpage.md (← 今，見ているこのファイル )
└── README.md (← slacs-webリポジトリについての説明mdファイル )
```

各年度の幹事は，基本的には `docs/index.md`, `docs/history/index.md` の情報を更新すれば良い．

