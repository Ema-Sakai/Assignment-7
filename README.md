# 概要
第7回課題の内容は下記の通り。
- DockerによるMySQL構築のハンズオン作業結果報告。  
ハンズオンは[こちら](https://github.com/raisetech-for-student/docker-mysql-hands-on "docker-mysql-hands-on")。
</br>

## 作業環境について
誰かの役に立ったら嬉しいので、私の作業環境を記載します。
- PC：Windows 11 Home
- バージョン：23H2
- システムの種類：64 ビット オペレーティング システム、x64 ベース プロセッサ
- プロセッサ：13th Gen Intel(R) Core(TM) i7-13700F   2.10 GHz
- 実装 RAM：32.0 GB
- ターミナル：PowerShell
- インストール作業日：2024/05/09
</br>

## 事前準備
Dockerのインストール。だがその前に、下記2点を先にインストールする必要があった。
- WSL2のインストール。
- Ubuntuのインストール。
</br>

> [!TIP]
> **WSL2とUbuntuのインストール手順は、下記動画を参考にした。**
> - [WSL2のインストールとセットアップ: 初心者向けガイド](https://youtu.be/gz-eOOyzSQE?si=D0mg4Kj6SxI14JFy "美濃加茂の蝮!")
> - [Windows11にWSL2をインストールする方法【授業では教えてません!!】](https://youtu.be/e3hg82e931k?si=Befhni_HsUbpQI_x "龍谷大学 先端理工学部 知能情報メディア課程")
> </br>
> 
> **Dockerのインストール手順は、下記サイトを参考にした。**
> - [Windows＋WSL2でDocker環境を用意しよう](https://www.kagoya.jp/howto/cloud/container/wsl2_docker/ "カゴヤのサーバー研究室")
>   - WSL2とUbuntuのことも記載があり、とってもわかりやすい。（最終更新日：2024/03/05）
</br>

## 作業結果報告
ハンズオンリポジトリを任意のディレクトリ配下にてcloneする。
![image](https://github.com/Ema-Sakai/Assignment-7/assets/166620990/e0fe4ff7-60bd-432b-ae08-2faf19124dc9)
</br>

`docker-mysql-hands-on`ディレクトリの作成と、`docker-compose.yml`があることを確認。
![image](https://github.com/Ema-Sakai/Assignment-7/assets/166620990/42ef4c40-e873-4114-8453-f2835a181700)
</br>

コンテナを起動したらエラーが返ってきた。  
緑線囲みのとおりDocker Desktop（アプリ）を管理者権限で直接実行し、再度コンテナを起動させた。  
その後無事に、`docker-mysql-hands-on`が存在していることを確認。
![image](https://github.com/Ema-Sakai/Assignment-7/assets/166620990/e2f0d1b3-26bc-4ff0-871b-40cb7be6b2a0)
![image](https://github.com/Ema-Sakai/Assignment-7/assets/166620990/092410ab-9b7d-475e-9f6c-da64d7cdb86c)
</br>

MySQLにログインを確認。  
※パスワードは`docker-compose.yml`の中身を別途確認。
![image](https://github.com/Ema-Sakai/Assignment-7/assets/166620990/eb56a69e-26e6-4a47-8298-ba19c8b63f48)
</br>

`movie_list`と`moviesテーブル`があることを確認。  
![image](https://github.com/Ema-Sakai/Assignment-7/assets/166620990/294da13f-eb62-4c9e-8b46-e7ab527ab066)
</br>

`moviesテーブル`のレコードを確認し、テーブルにレコードを追加及び結果確認。
![image](https://github.com/Ema-Sakai/Assignment-7/assets/166620990/d63edab3-323b-4415-9e30-1eaa89c64b0b)
</br>

MySQLからログアウトし、Dockerを停止及び停止の確認。
![image](https://github.com/Ema-Sakai/Assignment-7/assets/166620990/7f9887f3-b99d-4329-89e7-b42fb32b584a)
</br>

以上でハンズオンの全工程が完了です。
