# インストール

次のようなエラーに遭遇した．
```zsh
-> % python3 extract_scene.py example_scenes.py SquareToCircle -pl
/Users/hirofumi.shiba48/.pyenv/versions/3.7.6/lib/python3.7/site-packages/pydub/utils.py:165: RuntimeWarning: Couldn't find ffmpeg or avconv - defaulting to ffmpeg, but may not work
  warn("Couldn't find ffmpeg or avconv - defaulting to ffmpeg, but may not work", RuntimeWarning)
Traceback (most recent call last):
  File "extract_scene.py", line 168, in <module>
    main()
TypeError: main() missing 1 required positional argument: 'config'
```

virtualenvによる仮想環境状態（(venv)などのカッコがpromptの前に付いている状態）で
```zsh
-> % pip3 install ffmpeg
Collecting ffmpeg
  Downloading ffmpeg-1.4.tar.gz (5.1 kB)
Installing collected packages: ffmpeg
    Running setup.py install for ffmpeg ... done
Successfully installed ffmpeg-1.4
```
をしてこのエラーにぶつかったので，グローバル環境にも入れて見たら何故か治ってしまった．
```zsh
-> % brew install ffmpeg
```

全く同じエラーに遭遇した[このissueページ](https://github.com/3b1b/manim/issues/781)では「ffmpegのバージョンの互換性をなおしたらいけた」と書いてあったが，そっちの方が根本的解決なのかもしれない．

[戻る](home)