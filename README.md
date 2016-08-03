# lamp_vagrant_provisioning

## 概要
VagrantのprovisionでLAMP環境を作成する為のツールです。
vagrant upを実行した際にAnsibleのplaybookが適応されます。

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
※ [hosts](https://github.com/keita-nishimoto/playbook_lamp/blob/master/hosts)のIPアドレス及び、[Vagrantfile](https://github.com/keita-nishimoto/lamp_vagrant_provisioning/blob/master/Vagrantfile)のIPアドレスは適時好きな物に書換えて下さい。

初期状態で動作させるには本モジュールと同階層に[playbook_lamp](https://github.com/keita-nishimoto/playbook_lamp)をGitクロンしておく必要があります。
※下記のような状態にしておく必要があります。

```
├── lamp_vagrant_provisioning
├── playbook_lamp
```
