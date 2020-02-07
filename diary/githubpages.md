# GitHub Pagesの設定
<br>
GitHub Pagesでは[Jekyll](https://jekyllrb.com)を利用してWebサイトを作成している．私のGitHub repositoryに入っている設定用ファイルは以下の通り．
<details><summary>`_layouts : Jekyllの設定上この名前でなければならない．`</summary><div>
- `default.html` : [Jekyllのpages-themeのGitHub repository](https://github.com/pages-themes/midnight)からコピーして来て，[MathJaxの追加](mathjax)や[TikZJaxの追加](tikzjax)などを行った．
</div></details>
+ `_includes` : Jekyllの設定上この名前でなければならない．[HP](https://jekyllrb.com/docs/themes/#overriding-theme-defaults)参照．
    - `mathjax-v3.html` : `_layouts/default.html`に直接書くのではなく，追記する形で行った．
+ `assets/css` : Jekyllのpages-themeの設定上，この名前でなければならない．[このGitHub repository](https://github.com/pages-themes/midnight)の`README.md`参照．
    - `style.scss` : customで自分のstyleを追加するためのファイル．
- `_config.yml` : configurationのための変数を定義できる設定用ファイル．
- 404.md : この名前のファイルを作って，ファイル先頭に
```
---
permalink: /404.html
---
```
と書けば，これが404ページとして表示される．これをYAML front matterと読んで，Jekyllにspecial fileだと認識させるためのもの．詳しくは[公式document](https://jekyllrb.com/docs/front-matter/)へ．

[戻る](home)