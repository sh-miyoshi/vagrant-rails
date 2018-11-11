# vagrant-rails

## Overview

Windwos上にVagrantを使ってRuby on Rails環境を作るためのスクリプトです。  
コマンド3個でrailsのトップ画面を表示できます  
しかも、ソースの編集はWindows上で行えます！

## Prerequire

このプログラムの実行にはあらかじめWindows上にVagrantをインストールしておく必要があります。  
※ここだけはどうしても自動化できませんでした。  

各ダウンロードサイトから[VirtualBox](https://www.virtualbox.org/wiki/Downloads)と[Vagrant](https://www.vagrantup.com/downloads.html)をダウンロードして、インストールしてください

## Usage

コマンドプロンプトから環境を構築し、Ruby on Railsを立ち上げる方法の説明です。

- 変数ファイルの編集
  - command: `vi ansible/group_vars/all.yaml`
  - 解説: テキストエディタでansible/group_vars/all.yamlを開き、appNameの項目を自分のアプリ名に修正します ※初回のみ
- VMを起動
  - command: `vagrant up`
  - 解説: VMを起動します。※初回はansibleによる自動構築が走るので少し時間がかかります。
- railsの起動
  - command: `vagrant ssh -c "/opt/start-rails.sh"`
  - 解説: railsを起動します。
- アプリへのアクセスと編集
  - ブラウザで[http://localhost:3000](http://localhost:3000)にアクセス
  - data/\<your-app-name\>内にrailsのアプリケーションが同期しています

## Author

Shunsuke Miyoshi
