---
layout: default
title: コンピュータプログラムによる自動テストプレイ / Board Game Design Advent Calendar 2014(25日目) - Open Design Games
tw:
  description: 1.テストプレイ、あなたは何をテストする？ / 2.コンピュータで自動テストプレイ！ / 3.aglab - テストプレイフレームワーク
  image_url: 
---

この記事は、[Board Game Design Advent Calendar 2014](http://www.adventar.org/calendars/447)の25日目として書かれました。

皆さんこんにちは、Open Design Gamesの[fullkawa](https://twitter.com/fullkawa)です。これまで
『[Xan](http://fullkawa.github.io/open-design-games/products/xan.html)』
『[Water Walker](http://fullkawa.github.io/open-design-games/products/water_walker.html)』
といったゲームをデザイン・頒布してきました。  
そして、現在はゲームマーケット2015春に向けて『Grands-Tours(仮)』という自転車ロードレースをテーマにしたゲームを制作中です。

さて。まさかの大トリです…！(;ﾟДﾟ)  
これだけ錚々たるメンバーが集まったアドベントカレンダーの最終日が自分でいいのか？という戸惑いはありますが、自分がこの企画を知ったときはここしか空いてなかったのですよ。そんなヘタレはさておき。  

この記事では『コンピュータプログラムによる自動テストプレイ』について書きたいと思います。  

### 構成

1. [テストプレイ、あなたは何をテストする？](testplay_1_what_do_you_test.html)
2. [コンピュータで自動テストプレイ！](testplay_2_on_the_computer.html)
3. [aglab - テストプレイフレームワーク](testplay_3_framework.html)

### 想定する読者

上記1のページは、ゲームデザインに興味を持つ方全般に向けて書いたものです。  
一方、2, 3についてはプログラムに関する知識がないと理解が難しいかもしれません。  

…とは言っても、ボドゲクラスタの中にはプログラミングスキルを持った方が相当数いらっしゃるように見受けられます。ある程度の人数には最後まで読んでもらえるはずです！(と自分に言い聞かせる)。

### 謝辞

今回の企画の発起人である、I was gameのカレーさんに感謝です！  
そして、これまでの24回の記事を執筆された皆様にも感謝！  
非常にためになる記事が多く、一読者としても大いに楽しませて頂きました。

前置きが長くなりました。それでは始めましょう。


→ 1. [テストプレイ、あなたは何をテストする？](testplay_1_what_do_you_test.html)
