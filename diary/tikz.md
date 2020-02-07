# Tikzを使えるようにするまで
<br>
## TikZJaxとは

script tagで括ったTikZのcodeを，SVG codeに変換してくれるTikZJaxというcompilerがあった（[GitHub](https://github.com/kisonecat/tikzjax)，[HP](http://tikzjax.com/)）．このHPに仕組みの解説があるので，以下に噛み砕いた結果を書いていく．
[web2js](https://github.com/kisonecat/web2js)という同じくJim Fowlerさんが作っているcompilerで，TeXエンジンをWebAssemblyにcompileする．続いて$\LaTeX$ formatが読み込まれ，

```[tex]
\documentclass[margin=0pt]{standalone}
\def\pgfsysdriver{pgfsys-ximera.def}
\usepackage{tikz}
```

が実行される．こうしてscript tagで括られたTikZ環境のcodeが実行され．結果がdumpされる．[TikZ](https://en.wikipedia.org/wiki/PGF/TikZ)は[PGF](https://en.wikipedia.org/wiki/Progressive_Graphics_File)言語を利用した（？）画像生成マクロパッケージだから，dumpされた結果はPGFで書かれている．これをDVIに変換してから，SVGが生成される．ここまで，全てユーザのブラウザ上での消息であるとのことだ．