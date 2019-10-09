---
layout: post
title: 【経歴】Pythonベースでの案件・ポジション
date: 2019-10-09 00:00:00 +0900
description: Pythonを使ったプロジェクトの実績一覧です。
tags: [work, Python forエージェント, forエンジニア]
permalink: python
---
## 案件、実績
リンクがあるものはメディアに取り上げられたものです。
- [Corobanプロジェクト](https://www.eisai.co.jp/news/2019/news201973.html)
- [WarpDriveプロジェクト](https://warpdrive-project.jp/)
- ハードウェアインテグレーション・ソフトウェアテストオートメーションツール

### Coroban(0.5年: AIデータエンジニア)
医療機関ごとの過去の入院患者の看護記録などを学習し、それをもとに毎日の看護記録から個々の入院患者の転倒・転落リスクをスコア化し、リスクの高い患者を表示。
これを活用することで、医療関係者の業務の負担軽減やリスク評価の均質化・客観化などが期待できる。

というコンセプトのもと、自然言語処理技術に基づく人工知能エンジン「Concept Encoder」の実装部分と医療機関ごとのシステムインターフェース設計・実装、またデータモデルの構築設計とインテグレーションに従事。
自然言語処理＋人工知能エンジンを使っており、インターフェースはクライアントにより多種多様に対応。
開発支援ツールの作成や、プロジェクトとしてのシステム発足も。

#### 開発
VMとDockerベース、インフラはオンプレミス／クラウド（AWS）がメイン。クライアントに依存する。
開発支援ツールはPythonベース。画像切り出しやリアルタイム音声入力、IoTハードウェアへのアラート発信など。
トリガーやインターフェースはAPIコールやCronのようなスケジューラーによる。
クライアントベースでアプリ側を対応した際はPHPやRuby、もちろんPythonベースも合わせフレームワークに対応させる。

### WarpDrive(2年: AIデータエンジニア)
ユーザのウェブブラウザーの中でウェブ媒介型攻撃の観測・分析を行い、攻撃検知時には悪性ウェブサイトの閲覧をブロックし、ユーザーに警告やアドバイスを行う。
さらに、インターネット上に存在する同システムの並列化（情報集約・横断分析・新機能展開等）を繰り返し、最新のウェブ媒介型攻撃に対応する。

というコンセプトのもと、データ集約や通信などフロントーバックボーンを担当、
また協力者を集めるための施策にも着手。

#### 開発
データ集計から個人情報のマスキング、データクレンジングなど「集める」「使えるようにする」まで一貫、
システムや要望に合わせて投入できるよう改修する。PandasかR言語かはアーキテクトやレスポンス評価などで決定。
可視化や検索を容易にするためにデータ集積用のWebアプリ(パッケージ・OSS不問)とのインターフェースや運用相談にも対応。

システムが大規模なのでHadoopベースの分散処理システムの構築・運用保守にも従事。

### ハードウェアインテグレーション・セキュリティソフトウェアテストオートメーションツール(2年: QA/QE)
ハードウェアベンダーの製品に自社パッケージを組み込む、というもの。
ベンダー側の環境に依存するためPerl、 Python, Ruby, Java, NodeJSなど多岐に渡る。
パッケージインストールのための要件とテストツールは採用している技術が異なるため。

#### 開発
Seleniumサーバーを立ててE2Eテストを含む、
- 画面の項目が切り替わっていること
- 画面の項目とコンフィグファイルに差異がないこと
- エビデンスを取ること
など、GUI・CUI面の双方からアプローチする。

環境構築からアンインストールまで一貫し、ライセンスチェック（サーバー通信）も行う。