# このドキュメントで学ぶこと
このドキュメントでは次のことを学びます。
- git addとは何か？
- git commitとは何か？
- git pushとは何か？
- git pullとは何か？
## git addとは何か？
git addはディレクトリやファイルの追加、変更、削除等を作業エリアからステージングエリアに追加するコマンドです。ファイルのアップデート内容を次回コミット対象とするよう、Gitに指示します。 ただし、実際にはgit addコマンドだけではリポジトリに何も影響しません。git commitコマンドを実行するまで、変更が実際に記録されることはありません。
## git commitとは何か？
git commitはgit addによって追加されたのをローカルリポジトリに記録するコマンドです。コミットするときは、変更を簡潔に説明するコミットメッセージを含める必要があります。
※コミットメッセージの書き方についての詳細は[こちら](https://qiita.com/itosho/items/9565c6ad2ffc24c09364)に読んでください。
## git pushとは何か？
git pushはローカルリポジトリからのコンテンツをリモートリポジトリに送信するコマンドです。
## git pullとは何か？
git pull はリモートリポジトリから最新の状態をローカルリポジトリに反映するコマンドです。
## 動き方
![Screen Shot 2022-12-22 at 0 31 41](https://user-images.githubusercontent.com/28291036/208942373-289fdca1-50cf-42c6-ab83-98722aba1aba.png)

## デモ
* git add, git commit, git push
* git pull

### git add, git commit, git push
- README.mdを修正して```git status```で確認する　　

![Screen Shot 2022-12-22 at 1 38 16](https://user-images.githubusercontent.com/28291036/208957656-abccb5db-a448-4920-92a2-6651de1d23ec.png)

- README.mdを```git add . ```でaddする
- addしたREADME.mdをローカルリポジトリに```git commit -m commit-message```でcommitする
- README.mdをリモートリポジトリに```git push origin branch-name```でpushする  

![Screen Shot 2022-12-23 at 13 49 53](https://user-images.githubusercontent.com/28291036/209273178-0c9933a9-f159-4eb5-877a-46ffb03761b2.png)  

- pushされたファイルをGitHubに確認する  

![Screen Shot 2022-12-23 at 14 02 44](https://user-images.githubusercontent.com/28291036/209274308-dc8cb067-527f-4a84-b60d-2528686b1092.png)  

### git pull
- GitHubから直接README.mdを修正する  

![Screen Shot 2022-12-22 at 1 58 36](https://user-images.githubusercontent.com/28291036/208962019-be10b0f2-d5b5-49b3-b598-cb233c518af4.png)

- 修正したREADME.mdをpushする  

![Screen Shot 2022-12-23 at 13 58 44](https://user-images.githubusercontent.com/28291036/209273959-dfa711d2-1429-4c31-a493-a3198df45f6d.png)  

- ローカルから```git pull origin branch-name```でpullしてREADME.mdが修正されているのを```cat README.md```で確認する  

![Screen Shot 2022-12-22 at 2 02 49](https://user-images.githubusercontent.com/28291036/208962777-b49215a4-98e9-4750-b4ed-b6066dd7656a.png)

## 宿題
※この宿題はSlackに提出しないでくだいさい。
### 準備
* [こちら](https://github.com/reytech-co-jp/yume-project/blob/main/lessons/github/01-%E3%83%AA%E3%83%9D%E3%82%B8%E3%83%88%E3%83%AA%E3%82%AF%E3%83%AD%E3%83%BC%E3%83%B3%E3%83%96%E3%83%A9%E3%83%B3%E3%83%81.md#%E5%AE%BF%E9%A1%8C)の宿題が完了していること
### 概要
- ローカルからREADME.mdを以下のように修正する
  ```
  # hello-world
  My first repo
  My first commit
  ```
2. そのファイルをaddする
3. コミットメッセージに‘My first commitというメッセージをREADME.mdに書く’というメッセージを書く
4. 修正したREADME.mdをpushする
5. GitHubからREADME.mdを以下のように修正する
  ```
  # hello-world
  My first repo
  My first commit
  My second commit
  ```
6. コミットメッセージに‘My second commitというメッセージをREADME.mdに書く’というメッセージを書く
7. 修正したREADME.mdをpushする
8. ローカルからpullする
### どうなったら宿題が完了と言えるのか
* ローカルから修正したREADME.mdがGitにpushされている
* リモートから修正したREADME.mdがローカルにpullされている

