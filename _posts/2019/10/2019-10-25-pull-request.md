---
layout: post
title: GitHubに投げたプルリクをMerge
description: 普段CTOやリードエンジニアとして活躍されている3~4名の方に、Railsだけでなく、「Rails×〇〇」をテーマに、コアでマニアックな技術について熱く語って頂きます！最後に懇親会の時間も設けております。※懇親会では本物のシューマイ出します！！
categories:
  - tech
tags:
  - git
  - todo
img: common/research.jpg
---

まずはこの絵を覚えておいてほしいです。
順番は、merge->rebase の順番に実施しています。
これは後ほど解説します。

![merge]({{site.baseurl}}/{{site.data.path.img}}/2019/10/merge.png)
![rebase]({{site.baseurl}}/{{site.data.path.img}}/2019/10/rebase.png)
![squash]({{site.baseurl}}/{{site.data.path.img}}/2019/10/squash.png)

## 結論

git rebase で運用したい場合、**push した後はローカルファイルを削除すること。**

## 操作手順

1. 適当な変更をして commit する
1. push してプルリクする
1. 「create a merge commit」を選択（Merge pull request）
1. 承認して master に merge する
1. merge したブランチを削除
1. ローカルで pull する
   - この段階で merge の画像の状態になっている
1. 適当な変更をして commit する
1. push してプルリクする
1. 「Rebase and merge」を選択（Rebase and merge）
1. 承認して master に merge する
1. merge したブランチを削除
1. ローカルで pull する
   - この段階で rebase の画像の状態になっている
1. 適当な変更をして commit する
1. push してプルリクする
1. 「Squash and merge」を選択（Squash and merge）
1. 承認して master に merge する
1. merge したブランチを削除
1. ローカルで pull する
   - この段階で squash の画像の状態になっている

## 解説

ぱっと見、rebase と squash の違いが分からないですね。
これは軽度の開発だと squash の意味がないから[^1]ですが、本格的な検証をするためのうまい例題が思いつかないので、実際に当たってみないと説明が難しいです。
これは TODO で管理しておきますー！

## 注釈

[^1]: 【squash の意味がない】ローカル開発時もバグ修正などで切り戻す際に git squash を使うように、今回のようなたった 1 回のコミットログでは squash かどうかは判断できないです。