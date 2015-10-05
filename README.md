#provision_ansible_test

## 概要
Vagrantのprovisionでansibleを使う為のツールです。
vagrant upを実行した際にansibleのplaybookが適応されます。

※下記のサイトを参考にさせて頂きました。
http://www.moyashi-koubou.com/blog/vagrant_ansible_windows/

## 使い方

本リポジトリの直下で以下のコマンドを実行します。
```
vagrant up
```

結果としてprovisioning配下のplaybookの内容が適応されます。

### 注意
Vagrantfileにはchef/centos-6.5というboxを適応していますのでこの名前はご自身の環境に合わせて変えて下さい。
※boxの状態によってはcommonの処理の途中でエラーになります。

初期状態で動作させるには本モジュールと同階層に以下のリポジトリをGitクロンしておく必要があります。
https://github.com/keita-nishimoto/playbook_lamp
