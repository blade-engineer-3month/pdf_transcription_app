# PDF全文抽出GUIアプリ

Python + Tkinter + OCRで作成したPDF全文抽出GUIアプリです。

## 主な機能

- PDFからのテキスト抽出: PDFファイル内のテキストデータを直接読み取り
- OCR（光学文字認識）: PDF内に画像として保存されている文字（スキャンされた文書など）を、OCR技術を使ってテキストに変換
- 複数ファイルの一括処理: 複数のPDFファイルを一度に選択し、まとめて処理
- ドラッグ＆ドロップ対応: ファイル選択ダイアログだけでなく、ウィンドウにファイルを直接ドラッグ＆ドロップして追加することも可能
- 選べる出力形式: 抽出したテキストを.txtまたは.docx（Word）形式で保存可能

## セットアップ方法
1. Pythonのインストールを行う。

公式サイト: python.org

2. 必要なライブラリのインストール
コマンドプロンプトやターミナルを開き、以下のコマンドを一行ずつ実行して、必要なライブラリをインストールする
Shell
- pip install tk
- pip install tkinterdnd2
- pip install PyMuPDF
- pip install pdf2image
- pip install pytesseract
- pip install Pillow
- pip install python-docx

3. Tesseract-OCRのインストール
OCR機能を利用するために、Googleが開発したTesseract-OCRというソフトウェアのインストールが別途必要

Windowsの場合:
以下ページより、インストールを行う。
https://github.com/UB-Mannheim/tesseract/wiki

インストール中に「Additional language data」の項目で、Japanese（日本語）にチェックを入れる

インストール後、プログラムがTesseract-OCRを見つけられるようにPATHを通す設定が必要になる場合がある

macOSの場合:
Homebrewを使って簡単にインストール可能。
ターミナルで以下のコマンドを実行する

Shell
- brew install tesseract
- brew install tesseract-lang

4. Popplerのインストール (pdf2image用)
pdf2imageライブラリがPDFを画像に変換するために、Popplerというツールが必要

Windowsの場合:

こちらのブログ記事などを参考にPopplerをダウンロードし、解凍
https://github.com/oschwartz10612/poppler-windows/releases/

解凍したフォルダの中にあるbinフォルダへのパスを、システムの環境変数PATHに追加

macOSの場合:
Homebrewを使ってインストールする

Shell
- brew install poppler

5. プログラムの実行
上記全てのセットアップが完了したら、提供されたPythonスクリプト（.pyファイル）を保存する
コマンドプロンプトやターミナルでそのファイルがあるディレクトリに移動して、以下のコマンドで実行する

Shell
- python ファイル名.py

