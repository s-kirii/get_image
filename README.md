2020-7-24

"get\_image.py"をそのまま実行すれば検索ワードと保存名が聞かれて入力すればそのままダウンロードが開始されます。それぞれファイルの形式はjpgで、指定した保存名の末尾に0から順に数字をつけた名前で保存されます。

作ってるスクリプトと同じ階層のディレクトリに"get\_image.py"を置いて、スクリプト内で

import get\_image

などとすればAPI(ライブラリ、モジュール)として実行できます。  
プログラム本文で以下の様に実行してください。

imgsrc=get\_image.ImageScraping(file\_path="保存したいファイルのパス")  
imgsrc.download\_img(keyword="検索したい語句", file\_name="保存名") 

#課題点
-ダウンロードできる画像の上限がなぜか20個です。BeautifulSoupやrequests.get()の使用をちゃんと理解していないのでそこかと思われるが...

#2020-07-25  
-同じファイルネーム保存フォルダ内にあったらファイル名の番号を自動で変更する機能を追加しました。
-ダウンロードプロセス終了後取得した画像の数を表示する機能を追加しました。
