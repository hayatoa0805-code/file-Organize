概要
memo フォルダ内にある .txt ファイルを取得し、
・作成日を取得
・ファイル名の先頭に日付を追加
・年/月ごとのフォルダを自動作成
・対応するフォルダへ移動
を自動で行います。

使用技術
Python
os
shutil
glob
datetime
フォルダ構成


実装内容
glob を使用して .txt ファイルを取得
os.stat() でファイル作成日時を取得
datetime で日付へ変換
os.makedirs() でフォルダを自動生成
shutil.move() でファイル移動

実行前:

memo/
├── sample.txt
├── test.txt

実行後:

interview/
└── 2026年/
    └── 5月/
        ├── 2026年05月12日_sample.txt
        └── 2026年05月12日_test.txt
