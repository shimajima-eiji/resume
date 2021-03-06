# News
Gatsby + NetlifyCMSに移行しています。
jekyll + NetlifyCMSでも良さそうですが、今まで使えていたGitHub Pagesが使えなくなるので、思い切って刷新中……
現行だとコンテンツと表示を完全に分離できていない（動作上の問題はなし、管理の仕方の問題）ので、いったん切り分けるために試行錯誤のアプローチを変える。
そのため、今後の内容は[View(Jamstack)](https://github.com/shimajima-eiji/Jamstack)と[Contents(profile)](https://github.com/shimajima-eiji/profile)に分ける。

外部連携をするとGitHub Pages側でエラーになるので、同期は別リポジトリで実施するかもしれない。
本格的に移行する場合は告知します。

# What's this?
日本向けのエージェントサイトにGitHub就活・転職を推奨する企業さまが増えてきました。（私調べ）
そこで、時代の波に乗ろうと思ってGitHubの経歴で案件をゲットする！というひとりプロジェクトを去年発足しました。

私レベルの経歴でやってみた結果、結構なマッチングやスカウトをいただくようになりましたので、これから頑張ろうとしている方（私が受け持っている生徒さん含む）に向けて、
ある程度のベストプラクティスとバッドノウハウを発信します。

## 読者に求める前提条件
- エンジニアリングスキルがなくても、適正を示すことができる人
  - エンジニアリングスキルとは、人事がいうコミュニケーションスキルと同様、抽象化されているために人によって回答が異なります。
  - したがって、ほぼ確実に近いぐらい、その人にとっては具体的な、他の人から聞けば玉虫色の回答しかできません。（これをカルチャーフィットと呼ぶことがあります）
  - つまり、採用担当者とのフィーリングが大事です。現場は二の次です…。
- エンジニアリングスキルがあっても、対人、チーム、クライアントでコミュニケーションの方法を切り替えられる人
  - なにも営業をやれ、といっているわけではないです。相手にとって利のある人だと印象づけ、成果としても反映できることが求められます。
  - **スキルのミスマッチを自分の力不足**だと考える人がいますが、**モバイルアプリエンジニアにオシロスコープ使わせてハードウェア設計させますか？**という話ですので、凹まなくていいです。無理なもんは無理。
- 新しい事を貪欲に学ぶ意欲、力
  - せめてなにかの社外勉強会に積極的に参加していってください。何を言っているか分からないｄうちは大変ですが、言語やフレームワークが違ってもシステムは似たりよったりな事が多いので、門外漢でも比較的わかるようになります。
  - 1つの言語を極めましょう。極めやすい言語はRubyですが、専門性が高いということを意味します。
- ブログを道楽ではなく運用まで考えたい人

Qiitaの記事読んで楽しめるレベルの人なら問題ないです。
例外的に、**採用ご担当の方やエージェントさんは[固定ページ](https://shimajima-eiji.github.io/resume/readme)をメインに見ていってもらえればと思います。**

# Agenda
<!-- TOC -->

- [What's this?](#whats-this)
    - [読者に求める前提条件](#読者に求める前提条件)
- [Agenda](#agenda)
- [I want to use it too](#i-want-to-use-it-too)
    - [Advice](#advice)
- [How to use](#how-to-use)
- [Preview](#preview)
- [どうやってカスタマイズする？](#どうやってカスタマイズする)

<!-- /TOC -->

# History
[CHANGELOG.md](https://github.com/shimajima-eiji/resume/blob/master/CHANGELOG.md)を参照してもらえると！
[参考](https://github.com/shimajima-eiji/resume/issues/6)を使うことで更新が非常に楽になります。

実運用まで考慮するなら、`git commit`をフックするかスクリプトでやってしまうのが良いかと思います。

# I want to use it too
ありがたいことに、普及にあたって一緒にやってみようと言ってくださる方が増えています。
そこで、被採用側の目線で自身の強みをPRできる方法を検討しています。
エンジニアとしては凄腕だけどGitHubの仕様に明るくない方にも使ってもらえるように、基本的にシステマチックな仕組みにしていません。
ここで言うシステマチックとは、たとえばGitHubのChangelog機能やRelease機能といったGitHub固有のものです。
もちろん、使えるに越したことはありませんが……。

## Advice
手前味噌の記事で恐縮ですが、[GitHubリポジトリからの脱出](https://shimajima-eiji.github.io/resume/lecture/misoca#プログラマ向けゲームを作る技術)はgitコマンドのスキルアップにちょうど良いですよ。
ゲーム感覚で楽しみながらコマンドを試すことができます。
普段日常から使うか？というと疑問ですが、gitコマンドに対する苦手意識の払拭には良いハズ！

# How to use
[resumeリポジトリ](https://github.com/shimajima-eiji/resume.git)をcloneして_postsの中をいじるだけです。
必要な画像とかはassetディレクトリ以下に入っています。CSSもここなので、適宜いじってください。
また、この辺りを自分で設定するのが大変な方（エンジニアなど）はgithub pagesが標準で提供しているテーマがあるので、_config.ymlで呼び出してあげるとよいでしょう。
[github pagesで使えるテーマで作ったページ](https://shimajima-eiji.github.io)

私が使っているテーマはカスタムテーマです。
[(http://jekyllthemes.org/)]((http://jekyllthemes.org/))で気に入ったものを**zipでダウンロード**して展開し、**_postsの内容を書き換えていく**ことで簡単に気に入ったデザインを適用できます。
お節介ですが、お借りしたテーマについては著作権情報やダウンロード先を明記しましょう。間違っても自身の著作物だと言い張らないように。

jekyll自体のお話については[本ブログ](https://shimajima-eiji.github.io/resume/tags/#jekyll)で触れていきますので、そちらも参考にしてみてください。

# Preview
ページは3パターンあります。

- [トップページ](https://shimajima-eiji.github.io/resume/)
  - [ファイル](https://github.com/shimajima-eiji/resume/blob/master/index.html)
- [記事ページ](https://shimajima-eiji.github.io/resume/blog/gooday)
  - [ファイル](https://github.com/shimajima-eiji/resume/blob/master/_posts/2019/11/2019-11-01-gooday.md)
- [固定ページ](https://shimajima-eiji.github.io/resume/readme)
  - [ファイル](https://github.com/shimajima-eiji/resume/blob/master/_posts/archive/2019-01-01-readme.md)

記事ページと固定ページは見た目を変えているだけで、構造的にはpost.htmlを使っていますので骨子は同じです。
トップページだけindex.htmlを使っており、構造が異なります。

やっていることとしては、トップページ(index.html)の{{contents}}が記事一覧(グローバル変数site)を、記事ページ(_posts/...md)が_layout/post.htmlを使っているぐらいです。
SSIとかそういうレベルに落とし込むと、何となく全体の絵が見えるかなと。
なお、一番最初に呼び出されているファイルは_layout/default.htmlです。

# どうやってカスタマイズする？
とりあえずは[jekyll]()を見てもらうのが一番ですが、あのサイトを見てわかるのは**一度はjekyllで試行錯誤をした人**だと思いますので、本サイトではそもそも導入する人を想定して、jekyll関連のページではなるべく省略をしないように心がけています。
（jekyllタグがあるページです）

やや高度な事がやりたくなってから見ると意味がわかるかも知れません。
私もjekyllを本格的に使い始めてから「デバッグってどうすんだっけ？」とかで見始めたものです……。
