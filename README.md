vagrant-rails
====

# Overview
Windwos上にVagrantを使ってRuby on Rails環境を作るためのスクリプトです。  
コマンド5個でrailsのトップ画面を表示できます

# Prerequire
このプログラムの実行にはあらかじめWindows上にVagrantをインストールしておく必要があります。  
※ここだけはどうしても自動化できませんでした(申し訳ありません・・・)  

各ダウンロードサイトから[VirtualBox](https://www.virtualbox.org/wiki/Downloads)と[Vagrant](https://www.vagrantup.com/downloads.html)をダウンロードして、インストールしてください

# Usage
コマンドプロンプトから環境を構築し、Ruby on Railsを立ち上げる案での説明です。
+ vagrant box add centos7 https://github.com/holms/vagrant-centos7-box/releases/download/7.1.1503.001/CentOS-7.1.1503-x86_64-netboot.box ※初回のみ
+ /path/to/vagrant-rails/にdataという名前のディレクトリを作成 ※初回のみ
+ /path/to/vagrant-rails/ansible/group_vars/all.yamlの中のappNameの項目を自分のアプリ名に修正 ※初回のみ

+ vagrant up
+ vagrant ssh
+ ./run.sh

+ ブラウザで[http://localhost:3000](http://localhost:3000)にアクセス

# Stop the Server
サーバを止める際は以下のコマンドでできます。
+ ./stop.sh
+ exit ※exit from vagrant ssh
+ vagrant halt

# Author
Shunsuke Miyoshi