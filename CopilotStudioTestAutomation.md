# Copilot Test Automation (Copilot Studio 自動テストツール)
Copilot Studio で利用しているデータソースのファイルやテキストを入力することで、自動的にFAQ作成とCopilot Studio での出力までを自動化することができるソリューションです。

![image](https://github.com/user-attachments/assets/44d9a73c-9638-4d43-b6ec-e3f8f1563058)

> [!Note]
> こちらの[Xのポスト](https://x.com/geekfujiwara/status/1846485598070280596)で紹介しております。感想はぜひこちらへ！

## 利用方法
以下のように利用します。動画はこちらをご覧ください。

https://github.com/user-attachments/assets/1edec178-64ba-4075-b1fc-ec30b67223e1

ポイントを説明します。

FAQ はPDF またはテキストから作成することができます。AI Builder で作成しています。

![image](https://github.com/user-attachments/assets/5e4ec05c-f88e-44c1-8d7a-2f72eafed0b2)

作成したFAQの質問を元にテストを実行します。

テスト結果を自動的に取得して、作成したFAQの想定回答とテスト結果の応答を比較します。どちらの結果もDataverse に保存されています。

![image](https://github.com/user-attachments/assets/cb365ea5-341c-4add-a5fa-d4b082d6bf23)

テスト結果を優先というボタンを押すと、回答列が上書きされます。

![image](https://github.com/user-attachments/assets/d38fc5ee-4656-4b2b-b51e-4acb6c6cfd96)

完了したらテストケースの一覧の画面に遷移します。こちらから以前実行したテストケース毎に管理することができます。

![image](https://github.com/user-attachments/assets/31a4ea4c-c491-4b13-8bdd-1fdb69ffcdef)


## 前提条件
* Power Apps Premium のライセンスが本アプリ利用者に必要です。
* AI Builder のクレジットを消費します。クレジットがある環境でご利用ください。
* 認証なしで公開済みのCopilot に対応しております。

## ソリューション
[リリース](https://github.com/geekfujiwara/CopilotStudioToolKit/releases/tag/CopilotTestAutomation)から入手できます。

## 事前準備
### Copilot のシークレットの取得方法
Copilot にAPI 経由で接続を行うためにCopilot のシークレットを取得する必要があります。その取得方法は以下のとおり行います。

設定を開きます。
![001](https://github.com/user-attachments/assets/2273895d-61f2-461c-af76-c49e3f16cf1f)

セキュリティを開きます。
<img width="352" alt="002" src="https://github.com/user-attachments/assets/ca114de9-7d68-4885-8fb3-5c647f955c8f">

認証なしに設定します。
<img width="386" alt="003" src="https://github.com/user-attachments/assets/c08cecbe-ea14-4333-ac1c-c9c8a3134c0b">

問題なければ進みます。
<img width="409" alt="004" src="https://github.com/user-attachments/assets/70caf68e-2da3-45d8-b70e-d5b5280839c1">

シークレットを取得します。
<img width="452" alt="005" src="https://github.com/user-attachments/assets/ac3409e5-163f-4a4f-a57b-b4984eb4f4c8">

コピーします。
<img width="649" alt="006" src="https://github.com/user-attachments/assets/0a76c603-2eb3-442d-89d4-dd805c120148">

こちらをCopilot Test Automation アプリに貼り付けるようにしてください。

Copilot は公開しておいてください。

![image](https://github.com/user-attachments/assets/83f97625-d741-486c-bb89-89115174f84d)

公開していない場合、最新版でテストできません。また、公開が一回もされていない場合はテスト時にエラーメッセージが返ってきます。
![image](https://github.com/user-attachments/assets/96710fc5-d236-4745-a604-cbe46af851bb)

この場合は、Copilot の公開後、Copilot Test Automation アプリからテストを実行するようにしてください。
