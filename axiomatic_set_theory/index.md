<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

# Coqで公理的集合論
## 実装レポジトリ
(https://github.com/seisyuu-hantatsushi/implement_set_theory_in_coq)

## Coqとは
(https://coq.inria.fr/)

## 論理

## Gentzenのシーケント計算

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
