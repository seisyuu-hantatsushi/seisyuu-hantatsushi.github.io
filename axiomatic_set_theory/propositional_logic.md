<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax:{inlineMath:[['\$','\$'],['\\(','\\)']],processEscapes:true},CommonHTML: {matchFontHeight:false}});</script>
<script type="text/javascript" async src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML"></script>

# 命題論理
##  命題論理
命題(proposition)とは真か偽が必ず決まる問いである.
命題論理とは命題の意味的な真偽を問わず,形式的な真偽に着目し,命題の真偽を得る.
そのために,論理式を定義する.

## 論理式
1. 命題定数は論理式である. $\top$を真,$\bot$を偽とし,この2つを命題定数とする.
1. 命題変数は論理式である. 命題変数とは命題を形式的に$p,q,p_1,p_2,\dots,p_n,\dots$と記号で表したものである.
1. 論理式は命題変数,命題定数とこれらを結合する演算子(結合子)で構成されて,$A,B,A_1,A_2,\dots,A_n,\dots$で表す.演算子は以下の4つである.
   1. $\lnot$:否定
   1. $\land$:連言,論理積
   1. $\lor$:選言,論理和
   1. $\to$:含意  

## 演算子
形式的な演算により論理式の真偽を判定する.各演算子の規則は以下の通り.

### 否定
|$A$||$\lnotA$|
|---|---|---|
|$\top$||$\bot$|
|$\bot$||$\top$|

<a href="https://seisyuu-hantatsushi.github.io/axiomatic_set_theory/#%E5%BD%A2%E5%BC%8F%E8%AB%96%E7%90%86" class="btn">形式論理</a>
[形式論理](https://seisyuu-hantatsushi.github.io/axiomatic_set_theory/#%E5%BD%A2%E5%BC%8F%E8%AB%96%E7%90%86)
[Next](predicate_logic.md)
[Top](index.md)
