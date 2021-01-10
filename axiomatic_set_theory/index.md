<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

# Coqで公理的集合論
## 実装レポジトリ
https://github.com/seisyuu-hantatsushi/implement_set_theory_in_coq

## Coqとは
https://coq.inria.fr/

## 論理

## Gentzenのシーケント計算

## 集合論

### $\in$
集合論は要素(element)が集合(set,collection)に"属する"という関係と論理より出発する.

### 素朴な内包的記法
素朴に"集合"をこの世のあらゆる物の集まりと考える.  
集まりを規定する命題を$P(x)$とする.  
命題$P(x)$を満たす要素$x$を集めた集合を下記のように記述する.<br>
$$
  \{x|P(x)\}
$$
<br>これは,<br>  
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
