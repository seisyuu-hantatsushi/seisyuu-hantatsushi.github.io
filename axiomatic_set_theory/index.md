<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

# Coqで公理的集合論
## 参考文献
- 数学基礎論入門 前原昭二 ISBN 4-254-11396-X
- 数学の基礎 島内剛一 ISBN 978-4-535-60106-2
- 数学の基礎 集合・数・位相 齋藤正彦 ISBN 4-13-062909-3
- 形式論理と公理的集合論入門 福島正久 (ロアジス出版)
- 数理論理学 松本和夫 ISBN 978-4-32-001682-8
- 数学基礎論 新井敏康 ISBN 978-4-00-730459-0
- 論理と計算のしくみ 荻谷昌己 西崎真也 ISBN 978-4-00-006191-9
- 集合と位相 斎藤毅 ISBN 978-4-13-062958-4
- 集合・論理と位相 新井敏康 ISBN 978-4-489-02249-1
- 現代集合論入門 竹内外史 ISBN 978-4-535-60116-1
- Coq/SSReflect/MathCompによる定理証明:フリーソフトではじめる数学の形式化 萩原学 アフェルト・レナルド ISBN  978-4-627-06241-2
## 実装レポジトリ
[implement_set_theory_in_coq](https://github.com/seisyuu-hantatsushi/implement_set_theory_in_coq)

## Coqとは
[The Coq Proof Assistant](https://coq.inria.fr/)

## 形式論理
論理を記号に置き換え,形式的に操作を行い,論理が正しいかを確認することが目的である.

### 命題論理
命題(proposition)とは真か偽が必ず決まる問いである.
命題論理とは命題の意味的な真偽を問わず,形式的な真偽に着目し,命題の真偽を得る.
そのために,以下のように論理式を定義する.
1. 命題定数は論理式である. $top$を真,$bottom$を偽とし,この2つを命題定数とする.
1. 命題変数は論理式である.

### 述語論理

### Gentzen流自然演繹

## 集合論

### $\in$
集合論は要素(element)が集合(set,collection)に"属する"という関係と論理より出発する.<br>
$$
  x \in A
$$
<br>で$x$は$A$に属するとする.

### 素朴な内包的記法
素朴に"集合"をこの世のあらゆる物の集まりと考える.  
集まりを規定する命題を$P(x)$とする.  
命題$P(x)$を満たす要素$x$を集めた集合を下記のように記述する.<br>
$$
  \{x|P(x)\}
$$
<br>これは,
$$
  \exists y \forall x(x \in y \leftrightarrow P(x))
$$
<br>の$y$である.

### みんな大好きRussel's paradox
素朴な内包的記法において,命題を$P(x)$を$\forall x, x \not\in x$とすると.
$$
  \forall x(x \in y \leftrightarrow x \not\in x) \\
  y \in y \leftrightarrow y \not\in y
$$
となり,矛盾する.これは,要素と集合が明確に規定されていないため発生する.

### 型理論(theory of type)
要素と集合が明確でないため発生するRussel's Pardoxをその発見者自身のBertrand Arthur William Russellが解決するために構築した理論である.
Coqはこの型理論をもとにした数学証明支援器である.
まず,
<div style="text-align: center;">
  この世のすべての記号(文字,数字)を1階の対象(object of type 1)とする.
</div>
これから,
<div style="text-align: center;">
  1階の対象を要素として集めて,2階の対象(object of type 2)を作成する. これは,2階の対象は1階の対象の集合である.
</div>
つまり,
<div style="text-align: center;">
  $n$階の対象(object of type n)を要素として集めて,$n+1$階の対象を作成する. これは,n+1階の対象はn階の対象の集合である.
</div>
これにより,要素と集合が明確に規定されるため,Russel's paradoxを回避できる.
