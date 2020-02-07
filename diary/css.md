# サイトの見た目を整える

GitHub Pagesでは，Jeklly Themeというテンプレートを使ってサイトのスタイルを決める．これをマイナーチェンジするために，`_config.yml`という設定ファイルでいくつかの変数がいじれるようになっていたり，CSSの設定の変更や拡張が出来たりする．詳しくはこの[GitHub repository](https://github.com/pages-themes/midnight)参照．

- [このサイト](https://github.com/pages-themes/cayman/issues/29)を見て，ヘッダーの内容を少し調整して，なるべく余計な情報を削ってシンプルにした．
- [GitHub repository](https://github.com/pages-themes/midnight)の`README.md`を参考にして，`/assets/css/style.scss`というファイルを作って，
```[css]
---
---

@import "{{ site.theme }}";
```
を記述してから，CSS設定を書いた．

[戻る](home)