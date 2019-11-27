---
layout: post
title: 【11/19 渋谷開催】UnityとドコモAIエージェントAPIを使った音声対話デバイスハンズオン
description: 初開催！UnityとドコモAIエージェントAPIで、音声対話デバイスを作成してみよう！
categories:
  - lecture
tags:
  - 勉強会
img: 2019/11/unity.jpg
lecture: テスト
---
{{site.data.post.lecture}}

## 開催概要

```
日時：2019年11月19日（火）19:00-21:30（受付開始：18:30～）
会場：ドコモR&Dサテライトスペース
費用：無料
定員：25名
主催：株式会社NTTドコモ
運営協力：株式会社びぎねっと

タイムテーブル
時間|アジェンダ|
18:30-19:00 受付
19:00-19:10 ドコモAIエージェントAPIについて
19:10-20:40 ハンズオン
20:40-21:30 懇親会
```

いつものように、[公式ページ](https://sebastien.connpass.com/event/153339/)より。
![公式の扉絵]({{site.baseurl}}/{{site.data.path.img}}/2019/11/event_153339.jpg)

## NTT(docomo)さんの音声対応について

VR握手会のPVは面白いな！これUnityな
- クライアント
  - GUI: Agent craft
  - 自然対話記述言語: XAIML
- シナリオ: Speak

こんなにサクッとできるのね
この辺をヘッドレスにできたら激アツ！

音声サンプルがめちゃくちゃ多いな！
これをVtuberでも使えんじゃね？
普通に音声使いたいだけでもアリだ

## タブレットの検索デモ
どうせならユーザーの入力も音声で完結させたいですよね、
画面見せながらフォーカス（四角で囲んだり）するのもわかりやすくていい。
→音声で完結させるのは危険！変更処理が面倒くさい？設計とか視覚的な問題かなぁ、とは思うんだけど実績みたいね。

**あったらいいね、はあまりリーチにならないらしい。**だろうなぁ。

## 求人・提携募集
ソリューションテンプレートの考え方に基づく。ハッカソン向けの話かなぁ。

## ハンズオンと資料説明
ペラ冊子をベースにやります。
資料自体もちょっと手順が飛んでいますが、概ねついていける状態でした。
前半はある程度知ってる前提（知らなくてもついていける程度）の感覚です。

連携部分さえ何とかなっていればちゃんと動いてるのが見えます。
VR握手会の実装はこれを繰り返していい感じにやればいいんだ！という自信がつきます。

### 補足
音声合成がすばらしい！
[APIのリクエストに含めるだけで使える](https://docs.sebastien.ai/step4/voice_types/)のは便利すぎる！
これだけのためにAgentCraftを使っても良いかも知れない。

今回はUnityから呼んだけど、他でも呼ぶ方法はあるはず。

## 時間がかかったところ、ハマり所など
Unityの初期設定ですね……。
画面のUIとか初期登録だとかでちょっと時間がかかります。

あと、csファイルを編集する時にVisual Studioを起動しようとしてめちゃくちゃ時間がかかりました。
もうこれ無視して直接お使いのエディタを開くほうが早いです。
今回いじるのも`C:\Users\%USERNAME%\Documents\New Unity Project\Assets\Sebastien\Example\example.cs`[^1][^2]です。お手元の環境でも試してみてください。
マシンスペックにも依存しますが、非常に調子が良くないのでコーヒーを飲んで気長に待ちましょう。

うち、私がハマったのはrotateの設定を`O`fとしてしまったこと。回転角度なので`0`fが正しいですね。
テキストのフォントがOだったので0だと気付くのに時間がかかりました……。

## 全体所感
一人だと絶対ここまで行かないよなぁ、と感じられるハンズオンでした。
設定が細かいですね。Unity側の設定とAgent Craft側の設定が直感的ではなかったなと。
ハンズオンを進めていくうちに「このパラメーターを受け取った時にどうやってるいるか」という判別をやってるんだろう、というのが理解できてきたので、まずはそこまで到達すれば一皮むける印象です。
**逆に、これを人に教える事はできないな**と感じたのも事実です。

そもそも、今回は[^3]サンプルファイルを書き換えたぐらいなので、実践ではそのまま使えないです。
一人で環境構築すらできないです。[^4]

これを解決できれば、API設計に対するハードルを下げられる面白い環境だと思いますよ。


## 注釈
[^1]: 【C:\Users\...\example.cs】Windowsでデフォルト設定だとこうなります。
[^2]: 【%USERNAME%】これはログインユーザーを意味するシステム変数です。batファイルとかでよく使われます。
[^3]: 【今回は】今回も？下地が既に出来上がっている（サンプルを配布されているなど）プロジェクトは、初期設定でハマって使えない、と自信喪失して諦めるパターンです。今日のハンズオンもそうなるだろうという気がします。
[^4]: 【一人で環境構築できない】ハンズオンあるある。