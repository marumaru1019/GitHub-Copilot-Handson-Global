---
published: false                        # Optional. Set to true to publish the workshop (default: false)
type: workshop                          # Required.
title: GitHub Copilot Workshop              # Required. Full title of the workshop
short_title: GH Copilot Workshop                # Optional. Short title displayed in the header
description: This is a workshop for...  # Required.
level: beginner                         # Required. Can be 'beginner', 'intermediate' or 'advanced'
authors:                                # Required. You can add as many authors as needed      
  - Kaisei Tsujimoto
contacts:                               # Required. Must match the number of authors
  - katsujim@microsoft.com
duration_minutes: 20                    # Required. Estimated duration in minutes
tags: GitHub Copilot, javascript, python          # Required. Tags for filtering and searching
#banner_url: assets/banner.jpg           # Optional. Should be a 1280x640px image
#video_url: https://youtube.com/link     # Optional. Link to a video of the workshop
#audience: students                      # Optional. Audience of the workshop (students, pro devs, etc.)
#wt_id: <cxa_tracking_id>                # Optional. Set advocacy tracking code for supported links
#oc_id: <marketing_tracking_id>          # Optional. Set marketing tracking code for supported links
#navigation_levels: 2                    # Optional. Number of levels displayed in the side menu (default: 2)
#navigation_numbering: true             # Optional. Enable numbering in the side menu (default: true)
#sections_title:                         # Optional. Override titles for each section to be displayed in the side bar
#   - Section 1 title
#   - Section 2 title
---

# GitHub Copilot Workshop (初級編)

GitHub Copilot をこれから使い始める/使い始めたばかりの方を対象としたワークショップです。

## 事前準備

- GitHub アカウント
- GitHub Copilot Business の利用ライセンス
- Visual Studio Code
- Git クライアント（Windows 環境の場合は Git for Windows 等）
- node20 or later
- python 3.9 or later
- (そのほかお好きな言語の開発環境)

## 環境の準備

今回は Visual Studio Code（VSCode）を用いてワークショップを実施します。GitHub Copilot 拡張機能のインストールが必要になりますので、[こちら](https://code.visualstudio.com/docs/copilot/setup)のリンクを参考に拡張機能のインストールを実施してください。

---

# Exercise 1
## 事前準備

### ワークショップ用リポジトリのダウンロード
まずはこちらにある[ワークショップ用のリポジトリ](https://github.com/tenjoufire/ghcbws)からワークショップで利用するソースコード類をダウンロードしてください。
ソースコードのダウンロードには2通りの方法が利用可能です。おすすめは Git コマンドを利用する方法ですが、Zip ファイルのダウンロードも可能です。以下のどちらかの手順を実行してください。

<details>
<summary>Option1 Git コマンドの利用</summary>

1. GitHub のページからリポジトリの URL をコピーしてください。
![クローン URL のコピー](./assets/ex0_02.png)
2. GitHub Copilot の拡張機能がインストールされた VS Code を開き、左側のアイコンから「SOURCE CONTROL」を選択し、「Clone Repositry」をクリックしてください。
3. 1の手順でコピーした URL を出てきたテキストボックスに入力し、ソースコードのクローンを行ってください。
4. リポジトリの保存場所を選択するウィンドウで、ソースコード類を保存するお好きなディレクトリを指定してください。
5. クローン完了後、リポジトリを開くかどうかを選択するウィンドウが出た場合は「Open」をクリックしてください

</details>


<details>
<summary>Option2 Zip ファイルのダウンロード</summary>
GitHub のページから「Download ZIP」を選択し、ローカルの環境にソースコードをダウンロードしてください。その後、ZIPファイルを任意のディレクトリに展開してください。

![ソースコードダウンロード](./assets/ex0_01.png)

GitHub Copilot の拡張機能がインストールされた VS Code を開き、先ほど展開したフォルダを VS Code で開いてください。
</details>

どちらの方法で実施した場合でも以下のように、必要なソースコード類を開けていれば OK です。
![最初の画面](./assets/ex0_03.png)


## まずは GitHub Copilot を触ってみる

### ソースコード生成を体験してみよう

1. はじめに VS Code の Explorer の中から、「Exercise1」ディレクトリを開き、「FirstCopilot.py」をダブルクリックしてください。
2. 画面右側にソースコードの中身が表示されたら、6行目の最後にカーソルを持っていき`Enter`キーを押してみてください。
3. 薄いグレーの色で GitHub Copilot からの補完が確認出来たら、`tab`キーを押して GitHub Copilot からの提案を受け入れてください。
<div class="info" data-title="Note">

> GitHub Copilot の補完が出ない場合は、VS Code ウィンドウの右下の Copilot アイコンの状態を確認してみてください。「Status:Ready」となっている場合は、補完が出るまで少し待ってみてください。
</div>

<details>
<summary>提案の例</summary>

![提案の例](./assets/ex0_04.png)
</details>

<div class="task" data-title="追加課題">

> このプログラムは控除が考慮されていませんが、所得税が一律で20%かかることを考慮した給与計算のプログラムを提案してもらうにはどうすればよいか考えてみてください。

</div>

### プログラムを完成させ実行してみよう

1. 引き続き、`calc_salary`関数の続きを GitHub Copilot を使いながら実装していきましょう。
2. 今回は、標準入力から一日の労働時間を整数で入力し、標準出力で給料を出力するように実装してみてください。

<div class="tip" data-title="tip">

> GitHub Copilot から思った通りの提案が出ない場合は、何回かやり直してみたり、やりたいことをコメントでかいてみたり、実装の最初の部分（変数宣言など）を書いてみたりしてください。
</div>

<div class="info" data-title="note">

> GitHub Copilot の提案は同じものである場合もあれば異なる提案になる場合もあります。これは GitHub Copilot の裏側で生成 AI（Open AI のモデル）を利用しているためです。
</div>

<details>
<summary>実装の例</summary>

![実装の例](./assets/ex0_05.png)
</details>


3. 実装が完了したら、`Ctrl + S`でファイルを保存し、`Ctrl + Shift + @`で VS Code 上のターミナルを開いてください。
4. ターミナル上で `cd Exercise1`と入力し、ディレクトリを移動してください。
5. ターミナル上で `python3 FirstCopilot.py` と入力し、実装したプログラムを実行してください。

<div class="info" data-title="note">

> プログラムの実行に失敗した場合は、どこがおかしいのかを含めて GitHub Copilot に聞いて解決を図ってみてください。
</div>

## GitHub Copilot Chat を触ってみる
一度先ほど実装した python のプログラムは閉じ、同じディレクトリの中にある `TryCopilotChat.java` を開いてください。

---

# Exercise 2

## GitHub Copilot を利用し、簡単なアプリケーションを作ってみる

