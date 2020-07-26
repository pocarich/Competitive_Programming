# パソコン甲子園・情報オリンピック（競技プログラミング）ガイドライン

<br/>

## 0. はじめのはじめに

- あんなん真面目にやる気ねぇよって人はそっ閉じして、どうぞ。
- 高専プロコンやETロボコン等で仕事を任されているならそっちを優先しましょう。

<br/>

## 1. はじめに

- パソコン甲子園プログラミング部門や情報オリンピックのようなプログラムの問題を解いて順位を競うようなプログラミングコンテストを**競技プログラミング（競プロ）**と言います。

- 以下では対策を行っていくうえで、**AtCoder**と**AOJ**というサービスを活用します。とりあえず両方アカウント作成しておきましょう。

  <br/>

  - [AtCoder](https://atcoder.jp/) （初めての人はログイン後、[Practice](https://atcoder.jp/contests/practice) のA問題を解いて雰囲気をつかんでください）
  - [AOJ](http://judge.u-aizu.ac.jp/onlinejudge/) 
  - [AOJ-PCK（パソコン甲子園過去問）](http://aoj-pck.vsw.jp/) （ブラウザによってはうまく表示されないぽい？）
  - [AOJ/AtCoder-JOI（情報オリンピック過去問）](https://joi.goodbaton.com/) 

  <br/>

- 競プロ、AtCoderに純粋に興味がある人は以下参考

  - [勉強か？趣味か？人生か？─プログラミングコンテストとは](https://www.slideshare.net/iwiwi/wakate-web-14323842)
  - [レッドコーダーが教える、競プロ・AtCoder上達のガイドライン](https://qiita.com/e869120/items/f1c6f98364d1443148b3)
  - [AtCoderに登録したら次にやること～これだけ解けば十分闘える！過去問精選10問～](https://qiita.com/drken/items/fd4e5e3630d0f5859067)
  - [AtCoder（競技プログラミング）の色・ランクと実力評価、問題例](http://chokudai.hatenablog.com/entry/2019/02/11/155904)

<br/>

## 2. 参考サイト

　上記サイトに加え、以下

　- [パソコン甲子園 プログラミング部門 予選の傾向と対策](https://www.hamayanhamayan.com/entry/2018/10/01/014322)

<br/>

## 3. レベル1（予選突破まではいかなくとも健闘したい人向け）- AtCoderレート：灰、茶相当

### 全般

- オンラインジャッジの提出結果の意味

  - **AC（Accepted）**

    正解！！　次の問題に進みましょう。

  - **CE（Compile Error）**

    コンパイルエラー。文法にミスがないか、提出ページでの言語選択を間違っていないか等確認しましょう。

  - **RE（Runtime Error）**

    実行時エラー。原因は様々あります。よくある原因は配列サイズ不足や0除算などなど。デバッグ機能を活用しつつ原因を探りましょう。

  - **WA（Wrong Answer）**

    純粋に解法が間違っています。解法に穴がなかったか改めて考え直してみましょう。

  - **TLE（Time Limit Exceeded）**

    実行制限時間超過。計算量が多すぎて制限時間内に計算が終了しなかった場合に表示されます。基本的に<span style="color: red; ">**1秒当たりの計算量（専らループ回数）の上限は10<sup>8</sup>回**</span>です。計算量を削減できないか改めて解法を考え直してみましょう。

  - **MLE（Memory Limit Exceeded）**

    メモリ制限超過。膨大なサイズの配列（<span style="color: red; ">**int型で約10<sup>7</sup>以上？**</span>）を宣言したりすると表示される場合があります。無駄に配列サイズを大きくしていないか、配列を再利用できないか等、改めて考え直してみましょう。

<br/>

- C言語

  配列、多次元配列、if文、for文、多重for文、while文、文字列等の知識が必要

  また、以下のヘッダファイルの存在も知っておくこと

  - **<stdio.h>** ：入出力関数（printf, scanf, sprintf 等）

  - **<stdlib.h>**：汎用関数（atoi, atof, bsearch, qsort, abs 等）

  - **<string.h>**：文字列操作（strcpy, strcat, strlen, strcmp 等）

  - **<math.h>**：数学関数（M_PI, sin, cos, atan2, pow, sqrt, fmax, fmin 等）

    ※Visual StudioでM_PIを使用する際は、最初に**#define _USE_MATH_DEFINES **と記述

<br/>

- Visual Studioのデバッグ機能の使い方を覚えましょう。想定した結果が出力されず、ぱっと見でコードのミスがわからない場合はデバッグ機能を活用しましょう。[このサイト](https://itsakura.com/visualstudio-debug)ではデバッグ機能の簡単な使い方を説明しています。また、デバッグ実行時には実行時エラーが発生した場合にポップアップウィンドウの「無視」を選択することでエラー箇所を指摘してくれます（下図参照）。他にも細かい機能が様々あるので、ぜひ調べてみてください。

<br/>

![g0](img\g0.jpg)

<br/>

![g1](img\g1.jpg)

<br/>

- 浮動小数点数型

