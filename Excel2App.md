## 解決しなかった場合の問い合わせ管理アプリ作成
Dataverse 問い合わせテーブルを作成する元となるExcel ファイルを入手することができます。

Copilot エージェントが回答を行えなかった場合はユーザーの離脱に繋がり、満足度を低下させます。

次の改善につなげるために対応できなかったことについて人間が問い合わせを確認できるようにします。

問い合わせを記録するDataverse テーブルを作成する元となる[Excel ファイルを提供](https://github.com/geekfujiwara/CopilotStudioAppsandTextAutomation/releases/tag/CopilotInquiry)しています。

## 使い方

とてもシンプルで、ダウンロードしたExcel ファイルを用いてテーブルを作成し、モデル駆動型アプリを発行するだけです。

### テーブルの作成
テーブルの作成はPower Apps のメニューから行います。

![image](https://github.com/user-attachments/assets/08f3c002-ad9e-4b80-bd26-de0e3280c091)

### モデル駆動型アプリの作成
作成したテーブルからモデル駆動型アプリを作成します。

![image](https://github.com/user-attachments/assets/3901da9d-8386-48fc-b443-cde94f97d2fc)

作成が完了すると以下のようなモデル駆動型アプリが完成します。

![image](https://github.com/user-attachments/assets/e49e2839-6a4a-483c-a285-b7471de5cad5)


### Copilot から問い合わせの起票フローの作成
また、ご自身のCopilot に問い合わせの起票機能を追加するにはトピックを作成します。

![image](https://github.com/user-attachments/assets/c07aef10-e2ad-45a1-9a95-808b90297d6a)


フローを作成してDataverse に登録するようにします。

![image](https://github.com/user-attachments/assets/c354275f-dc5f-4830-b58f-a27452ef39f5)


### トピックに関連付ける
`解決しなかった`を選択した際に問い合わせに流れるようにします。

![image](https://github.com/user-attachments/assets/7bf9c1f6-9b22-466d-bd96-64973c3279e4)


こちらで問い合わせを起票することができます。

[ルートページへ](https://github.com/geekfujiwara/CopilotStudioToolKit)
