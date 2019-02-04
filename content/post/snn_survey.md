---
title: "WIP:SNNのさーべい"
date: 2019-02-04T16:44:52+09:00
publishdate: 2019-02-04
lastmod: 2019-02-04
draft: false
tags: []
---

# introduction to spiking neural networks: information processing, learning and applications
SNNのサーベイ的な論文を読んでメモる.
僕は神経科学とか機械学習の素人なのでいろいろあれかも

# 概要
SNN(Spiking Neural Network)はニューロンがスパイクするダイナミクスをモデル化した人工ニューラルネットワーク．

# スパイクの特徴
* ニューロンは複数の入力から一つのスパイクシグナルを出力する
* 興奮性，抑制性入力により発火の可能性をコントロールできる
* ニューロンは1つ以上の内部状態により管理されていて，それが閾値を超えると発火する

# ネットワークトポロジ
## Feedforward networks
入力と出力の方向が1方向である．フィードバックがない．生体では脳の表面近くの組織で多く見つかる．  
このネットワークは低レベルな感覚器官
## Recurrent networks
フィードバックもあるネットワーク．フィードバックにより，一時的で動的な発火が行われる．Feedforward networksより高級で演算性能に優れる．その分，学習とコントロールが難しい．
## Hybrid networks
このネットワークはFeedforward networksとRecurrent networksを持つことができるネットワーク．方向が単方向または双方向な場合もある．
### Synfire chain
人間の学習は2つのイベントが相互関係を持っていたり，シグナルとその後の行動が結びついていることがしばしばある．  
イベントは時間で分割できるが，正確に正しいタイミングで正しい行動を予測するために，人間はこれらをリンクさせる．
synfireは遅延イベントを表現している．sinfire chainはチェインを組み合わせる複数レイヤのアーキテクチャである．これはニューロンの発火を同期的な波として他のレイヤに伝える．
### Reservoir computing
これはRecurrent networksの演算性能を活かしつつも，学習の難しさを克服したものである．
あとで[よむ](https://qiita.com/kazoo04/items/71b659ced9dc0342a2b0)

# Spiking Neuronにおける情報処理
毎ミリセカンドごとに感覚器官から出力される膨大なスパイクを，感覚器官の刺激から行う行動を決定するために，これらを脳は処理する．
## Neural code
neural codeはニューラルシグナルでの情報のエンコーディング．
firing rateが重要視されてきたが，timing 
