## PDF・画像のテキストファイル化
PDFや画像形式のファイルは構造上の問題によりナレッジソースとして動作しないケースがあります。その際にはテキストファイル化を検討してください。

[こちら](https://github.com/geekfujiwara/CopilotStudioAppsandTextAutomation/releases/tag/TextFileConverter)からダウンロードできます。

以下のようなPower Automate のフローが入っています。SharePoint ドキュメントライブラリとインプット用とアウトプット用のフォルダを作成しておき、インプットに画像またはPDFファイルが入れば自動的にアウトプットフォルダに保存されます。

![image](https://github.com/user-attachments/assets/9caf71b7-28ae-4001-a176-0ad042db4917)

出力されたテキストファイルはCopilot Studio のデータソースとして利用することができます。

SharePoint に配置するか、アップロードしたドキュメント機能で利用しましょう。

## 制限事項
ファイルサイズが20MBを超える場合は処理をスキップします。その場合、20MB以下にファイルを分割するようにしてください。

> [!Note]
> 例えばPDFであれば一部のページを印刷機能を用いて分割することなどが行えます。またPower Automate for desktop を利用すれば分割アクションを利用できます。


### インストール方法
環境変数を4つ設定する必要があります。

![image](https://github.com/user-attachments/assets/77e446f0-283b-4fe2-86a2-5845dfd00ba3)

SharePoint ドキュメントライブラリを用いてファイルの変換を行うため、ドキュメントライブラリを作成/既存利用し、2つのフォルダ(インプット用、アウトプット用)を作成してそのフォルダ名等を環境変数に設定します。

![image](https://github.com/user-attachments/assets/f8e65c19-0428-4934-bf46-f62cdb0a6375)

SharePoint サイトのURL 取得します。開いている状態でここまでのURLがサイトのURLになります。

こちらを環境変数の `SharePoint Site URL` に設定します。

"https://xxxxx.sharepoint.com/sites/Microsoftdemo" のように入力します。

![image](https://github.com/user-attachments/assets/3d6245ee-a936-4014-b4ad-2560d4e450ba)


このようにSharePoint ドキュメントライブラリ名とフォルダ名を確認しておきます。この例ですと、SharePoint ドキュメントライブラリ名 `TextConverter` とフォルダ名 `Input`, `Output` が必要となります。

これらを環境変数 `SharePoint Library Name`, `Input Folder Path` , `Output Folder Path` に設定します。



`Input Folder Path` は以下のように設定します。

![image](https://github.com/user-attachments/assets/82dad4fc-2723-4ac4-8754-b3fa6caa0b1a)

`Output Folder Path` は以下のように設定します。

![image](https://github.com/user-attachments/assets/100b9166-90a2-4326-8ce7-5ab429d4e61a)

`SharePoint Library Name` は以下のように設定します。

![image](https://github.com/user-attachments/assets/9073318b-809e-4226-943f-3b64483f6a77)


ルートページへ
