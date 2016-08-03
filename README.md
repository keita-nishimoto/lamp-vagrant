# lamp_vagrant_provisioning

## 概要
VagrantのprovisionでLAMP環境を作成する為のツールです。
vagrant upを実行した際にAnsibleのplaybookが適応されます。

[Qiita](http://qiita.com/)のほうで環境構築に関する記事を書いてあります。

- [LAMP 環境構築 PHP 7 MySQL 5.7（前編）](http://qiita.com/keita-nishimoto/items/5441244604fbc6db7907)
- [LAMP 環境構築 PHP 7 MySQL 5.7（後編）](http://qiita.com/keita-nishimoto/items/7d0a8d6e24c1861d799f)

## 事前準備
Ansibleのインストールを行います。

```
$ brew install ansible
```

## 使い方

本リポジトリの直下で以下のコマンドを実行します。
```
$ git clone https://github.com/keita-nishimoto/playbook_lamp.git
$ vagrant up
```

結果として[playbook_lamp](https://github.com/keita-nishimoto/playbook_lamp)配下のplaybookの内容が適応されます。

### 注意
※ [インベントリファイル](https://github.com/keita-nishimoto/playbook_lamp/blob/master/local)のIPアドレス及び、[Vagrantfile](https://github.com/keita-nishimoto/lamp_vagrant_provisioning/blob/master/Vagrantfile)のIPアドレスは適時好きな物に書換えて下さい。

初期状態で動作させるには本モジュールと同階層に[playbook_lamp](https://github.com/keita-nishimoto/playbook_lamp)をGitクロンしておく必要があります。
※下記のような状態にしておく必要があります。

```
├── lamp_vagrant_provisioning
├── playbook_lamp
```
