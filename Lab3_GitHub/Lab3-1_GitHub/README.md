# Dojo Basic: Lab3-1 GitHub基礎

## 目的とゴール
### 目的
 - GitHubを使ったコード、ドキュメント管理を体験します。

### ゴール
 - GitHubでコード、ドキュメントの管理、共同作業を行える様にする。

### このLabの実施前提
 - GitHubのアカウントを持っていること
 
### このLabで体験できること
 - GitHubでレポジトリー(Repository), README.mdを作成
 - ブランチ(Branch)を作成、README.mdを編集
 - コミット(Commit), プルリクエスト(pull Request)を行う
 - 他の人のrepository からfork
 - コードを修正、Pull Requestを行う
 
 参照
- GitHub ウェブサイト　https://github.com/
- 本日の元ネタ(英語)　https://guides.github.com/activities/hello-world/?fbclid=IwAR2fRgqDpfDh5vUCeYrP_HbNZhT6MoVnFqgRztJoJD0u3QSmSzOC7ieqiRI

# GitHubとは
GitHubは、ソースコードのバージョン管理ツール、"Git"を利用した開発者を支援するWebサービスで、
バージョン管理とコラボレーションのためのコードホスティングプラットフォームです。GitHub を使えば、どこにいてもプロジェクトで他の開発者と一緒に作業することができます。

OSSの例
- Linux (https://github.com/torvalds/linux)
- Kubernetes (https://github.com/kubernetes/kubernetes)
- OpenWhisk (https://github.com/apache/openwhisk)
- Node-Red (https://github.com/node-red/node-red)
- Ruby (https://github.com/ruby/ruby)

このチュートリアルでは、リポジトリ、ブランチ、コミット、プルリクエストといった GitHub の基本的なことを学びます。Hello World リポジトリを作成し、GitHub の Pull Request ワークフローを学びます。

このチュートリアルを完成させるには、GitHub.com のアカウントとインターネットへのアクセスが必要です。コードの書き方やコマンドラインの使い方、Git (GitHub の上に構築されたバージョン管理ソフトウェア) のインストールなどの知識は必要ありません。

# Step 1. Repository(リポジトリー)を作成する
リポジトリは通常、一つのプロジェクトを整理するために使用されます。リポジトリには、フォルダやファイル、画像、ビデオ、スプレッドシート、データセットなど、プロジェクトに必要なものは何でも入れられます。最初にプロジェクトに関する情報をまとめたファイル、READMEを用意することをお勧めします。また、ライセンス情報なども入れておくといいでしょう。
- (参考　企業でのOSS活用とOSSライセンス、　https://www.ibm.com/downloads/cas/VW0PZRBO　）

これから最初のレポジトリ　”hello-world”を作っていきましょう。

## 新しいリポジトリを作成するには
- GitHubページ(https://github.com/)にログインしてください。
- 画面の左上にご自分の名前、"Repositories"の右側の"New"をクリックしてください。

<kbd><img src="images/github1-1.png" width="300px"></kbd>

- リポジトリの名前を hello-world とします。
- このリポジトリを README で初期化するを選択します。
- "Create Repository"をクリックしてください。

<kbd><img src="images/github1-2.png" width="640px"></kbd>



#  Step 2. ブランチを作る
ブランチとは、リポジトリの異なるバージョンの作業を行う方法です。

デフォルトでは、リポジトリには masterという名前のメインブランチがあります。masterブランチにコミット(書き込み）する前にデバッグ、テストをしたり、編集をしたりするためにブランチを使います。

masterブランチからブランチを作成するときは、その時点での masterのコピー、つまりスナップショットを作成することになります。あなたがブランチで作業をしている間に誰かがメインブランチに変更を加えた場合でも、その更新を取り込むことができます。

この図を見てください。

- masterブランチ
- readme-edits という名前の新しいブランチ
- 修正をmainブランチに統合するまでの流れ

<kbd><img src="images/github2-1.png" ></kbd>

共同作業でファイルの異なるバージョンのファイルを保存したことがありますか？　例えると以下のようにファイル名を変えて管理していくような感じです。

- story.txt
- story-test.txt
- story-202008.txt
ブランチは、GitHub のリポジトリでも同じような目的を達成することができます。

ここGitHubでは、開発者、ライター、デザイナーがブランチを使ってバグ修正や機能追加の作業をメインブランチとは別に行っています。変更の準備ができたら、ブランチをメインブランチにマージします。

## 新しいブランチを作る
リストの左上にある branch: main というドロップダウンをクリックします。
- 新しいブランチのテキストボックスにブランチ名を readme-edits と入力します。
- Create branch readme-editsをクリックしてください。

<kbd><img src="images/github2-2.png" width="400px"></kbd>

ブランチが"readme-edits"に変わったのがわかります。README>mdの内容は変わりません。
<kbd><img src="images/github2-3.png" width="640px"></kbd>

これでmainとreadme-editsの2つのブランチができました。見た目は全く同じですが、次に新しいブランチに変更点を追加します。

# Step 3. 変更してコミットしましょう
では、編集をしてみましょう。

GitHub では、編集して保存することをコミットと呼びます。それぞれのコミットにはコミットメッセージが付きます。コミットメッセージには変更の履歴が記録されているので、他の投稿者はあなたが何をしたのか、なぜ変更したのかを理解することができます。

変更の作成とコミット
- 1 ファイルビューの右上にある鉛筆のアイコンをクリックして編集します。
<kbd><img src="images/github3-1.png" width="640px">

- 2 何か文章を追加してみてください。内容は何でもいいです。
<kbd><img src="images/github3-2.png" width="640px"></kbd>

- 4 追加した内容にコメントを書いておきましょう。
<kbd><img src="images/github3-3.png" width="640px"></kbd>

- 5.変更をコミットするボタンをクリックします。
<kbd><img src="images/github3-4.png" width="640px"></kbd>

これらの変更は readme-edits ブランチの readme ファイルだけに行われるので、このブランチには main とは異なる内容が含まれます。

# Step 4. プルリクエストする
もう少し頑張りましょう。 main 以外のブランチに変更を加えたので、プルリクエストを開いてみましょう。

プルリクエストは、GitHub での共同作業の中心となるものです。プルリクエストを開くと、あなたの変更点を提案し、誰かがあなたの投稿を確認してプルインして自分のブランチにマージすることを要求していることになります。プルリクエストには、両方のブランチの内容の差分が表示されます。変更、追加、削除は緑と赤で表示されます。

コミットしたらすぐにプルリクエストを開いて、コードが完成する前から議論を始めることができます。

GitHub の @mention システムをプルリクエストのメッセージに使えば、特定の人やチームにフィードバックを求めることができます。

- pull requestを選択、　
- "Create a pull request"をクリックしてください。

<kbd><img src="images/github4-1.png" width="640px"></kbd>

今回のプルリクエストに関するコメントを書いてください。
<kbd><img src="images/github4-2.png" width="640px"></kbd>

"Create a pull request"でmainブランチへの変更依頼(pull request)を遅れます。

# Step 5. プルリクエストを取り込む（マージする）
この最後のステップでは、あなたの変更をまとめる時が来ました - readme-edits ブランチをメインブランチにマージします。

- mainブランチを選択してください

<kbd><img src="images/github4-3.png" width="640px"></kbd>
- "Pull requests"を選択してください。先ほどのプルリクエスト"Update README.md"をクリックしてください。
<kbd><img src="images/github4-4.png" width="0px"></kbd>
- 問題なければ"Merge pull request"をクリックしてください
<kbd><img src="images/github4-5.png" width="640px"></kbd>
- "Confirm merge"をクリックしてください

<kbd><img src="images/github4-6.png" width="400px"></kbd>
- readme.editsでの変更が反映されましたね。

<kbd><img src="images/github4-7.png" width="640px"></kbd>

お疲れ様でした!
このチュートリアルが完了したことで、プロジェクトを作成して GitHub でプルリクエストを行う方法を学びました。

このチュートリアルで達成したことは次のとおりです。

- リポジトリを作成する
- 新規ブランチの作成
- ファイルを変更し、その変更を GitHub にコミットしました。
- プルリクエストのオープンとマージ

Pull Requests の力について詳しく知りたい場合は、GitHub のフローガイドを読むことをお勧めします。また、GitHub Explore にアクセスしてオープンソースプロジェクトに参加してみるのもいいかもしれません。

https://guides.github.com/introduction/flow/

# フォーク
フォークとはリポジトリのコピーのことです。 リポジトリをフォークすることにより、オリジナルのプロジェクトに影響を与えることなく変更を自由にテストできます。
またコピーした後にオリジナルの他の人の作ったコードにプルリクエストを出して変更を取り込んでもらうことも可能です。

GitHubにサインインした後にへターゲットのレポジトリーに行ってください。　（ここでは例としてhttps://github.com/osonoi/hello-world2)
"osonoi"と言うアカウントの"Hello-world"をフォークします。

こちらのIBMの開発者向けのコードパターンもオープンソースで公開されています。フォークして活用してください。 <br>
https://developer.ibm.com/jp/patterns/

それぞれの記事の"README"をクリックするとGitHubのページにいくことができます。　<br>
- スケーラブルな WordPress 実装を Kubernetes 上にデプロイする  https://github.com/IBM/Scalable-WordPress-deployment-on-Kubernetes/blob/master/README.md
- 教育用のセルフサービス・チャットボットを作成する https://github.com/IBM/Education-SelfService-AI-Chatbot/blob/master/README.md

右上にある"Fork"をクリックしてください。

<kbd><img src="images/fork1.png" width="640px"></kbd>
- フォークが始まります。(ここではymatsunamiと言うアカウントでログインしています）

<kbd>v<img src="images/fork2.png" width="640px"></kbd>

- 先ほどのレポジトリーが自分のレポジトリーとして編集できるようになりました。右側のペンのアイコンをクリックして編集しましょう

<kbd><img src="images/fork3.png" width="640px"></kbd>

- 新しいテキストを入力します。

<kbd><img src="images/fork4-edit.png" width="640px"></kbd>

- 変更をコミットします。

<kbd><img src="images/fork5-commit.png" width="640px"></kbd>

- 変更が反映されましたね。ご自分（ここでは(ymatsunami)のレポジトリーの内容が変更されました。

<kbd><img src="images/pull-req1.png" width="640px"></kbd>

## プルリクエストを出す場合
- "Pull-request"をしてみましょう。上のメニューから"Pull-requests"を選んで

<kbd><img src="images/pull-req2.png" width="640px"></kbd>

- "Create pull resuest"をクリック

<kbd><img src="images/pull-req3.png" width="640px"></kbd>

- コメント追加して"Pull request"をクリック

<kbd><img src="images/pull-req4.png" width="640px"></kbd>
