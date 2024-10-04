# Copilot Studio 便利ツール郡
Copilot Studio 利用するにあたって便利ツールを共有しています。

今後 Copilot 改善ソリューションに統合も検討していますが、単一ツールとして利用したい場合もありますので並行して提供していきます。

# ツール
## PDF・画像のテキストファイル化
PDFや画像形式のファイルは構造上の問題によりナレッジソースとして動作しないケースがあります。その際にはテキスト化を検討してください。
[こちら](https://github.com/geekfujiwara/CopilotStudioAppsandTextAutomation/releases/tag/TextFileConverter)からダウンロードできます。

### インストール方法
環境変数を4つ設定する必要があります。

SharePoint ドキュメントライブラリを用いてファイルの変換を行うため、ドキュメントライブラリを作成/既存利用し、2つのフォルダ(インプット用、アウトプット用)を作成してそのフォルダ名等を環境変数に設定します。

![image](https://github.com/user-attachments/assets/77e446f0-283b-4fe2-86a2-5845dfd00ba3)

SharePoint サイトのURL 取得します。開いている状態でここまでのURLがサイトのURLになります。

こちらを環境変数の `SharePoint Site URL` に設定します。

![image](https://github.com/user-attachments/assets/3d6245ee-a936-4014-b4ad-2560d4e450ba)


このようにSharePoint ドキュメントライブラリ名とフォルダ名を確認しておきます。この例ですと、SharePoint ドキュメントライブラリ名 `TextConverter` とフォルダ名 `Input` `Output` が必要となります。

これらを環境変数 `SharePoint Library Name`, `Input Folder Path` , `Output Folder Path` に設定します。

![image](https://github.com/user-attachments/assets/f8e65c19-0428-4934-bf46-f62cdb0a6375)

`Input Folder Path` は以下のように設定します。

![image](https://github.com/user-attachments/assets/82dad4fc-2723-4ac4-8754-b3fa6caa0b1a)

`Output Folder Path`

![image](https://github.com/user-attachments/assets/100b9166-90a2-4326-8ce7-5ab429d4e61a)

`SharePoint Library Name`

![image](https://github.com/user-attachments/assets/9073318b-809e-4226-943f-3b64483f6a77)



## 解決しなかった場合の問い合わせ管理アプリ作成
Dataverse 問い合わせテーブルを作成する元となるExcel ファイルを入手することができます。

Copilot エージェントが回答を行えなかった場合はユーザーの離脱に繋がり、満足度を低下させます。

次の改善につなげるために対応できなかったことについて人間が問い合わせを確認できるようにします。

問い合わせを記録するDataverse テーブルを作成する元となる[Excel ファイルを提供](https://github.com/geekfujiwara/CopilotStudioAppsandTextAutomation/releases/tag/CopilotInquiry)しています。
