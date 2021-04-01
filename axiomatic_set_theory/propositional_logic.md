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
1. 論理式は演算子により結合され,結合されたものも論理式である.

## 演算子
形式的な演算により論理式の真偽を判定する.各演算子の真理値表は以下の通り.

### 否定(negation)

|$A$||$\lnot A$|
|----|----|----|
|$\top$||$\bot$|
|$\bot$||$\top$|

### 連言,論理積(conjunction)

|$A$|$B$||$A \land B$|
|---|---|---|---|
|$\top$|$\top$||$\top$|
|$\top$|$\bot$||$\bot$|
|$\bot$|$\top$||$\bot$|
|$\bot$|$\bot$||$\bot$|

### 選言,論理和(disjunction)

|$A$|$B$||$A \lor B$|
|---|---|---|---|
|$\top$|$\top$||$\top$|
|$\top$|$\bot$||$\top$|
|$\bot$|$\top$||$\top$|
|$\bot$|$\bot$||$\bot$|

### 含意(implication)

|$A$|$B$||$A \to B$|
|---|---|---|---|
|$\top$|$\top$||$\top$|
|$\top$|$\bot$||$\bot$|
|$\bot$|$\top$||$\top$|
|$\bot$|$\bot$||$\top$|

### 同値(equivalence)

$(A \to B) \land (B \to A)$の略号を$\leftrightarrow$とし同値という.

|$A$|$B$||$A \leftrightarrow B$|
|---|---|---|---|
|$\top$|$\top$||$\top$|
|$\top$|$\bot$||$\bot$|
|$\bot$|$\top$||$\bot$|
|$\bot$|$\bot$||$\top$|

### 演算子の結合順位

1. $\lnot$
1. $\land,\lor$
1. $\to$
1. $\leftrightarrow$

## 恒真式(tautology)
命題変数の真偽に関わらず,論理式の真理値の結果がすべて真なるとき,この論理式を恒真式という.
モーダスポネンス(Modus Ponens,MP)$((P \to Q) \land P) \to Q$は恒真式である.

|$P$|$Q$|$P \to Q$|$(P \to Q) \land P$||$((P \to Q) \land P) \to Q$|
|---|---|---|---|---|---|
|$\top$|$\top$|$\top$|$\top$||$\top$|
|$\top$|$\bot$|$\bot$|$\bot$||$\top$|
|$\bot$|$\top$|$\top$|$\bot$||$\top$|
|$\bot$|$\bot$|$\top$|$\bot$||$\top$|

<input type="button" onclick="location.href='https://seisyuu-hantatsushi.github.io/axiomatic_set_theory/#%E5%BD%A2%E5%BC%8F%E8%AB%96%E7%90%86'" value="形式論理">
[Next](predicate_logic.md)
<input type="button" onclick="location.href='[https://seisyuu-hantatsushi.github.io/axiomatic_set_theory" value="TOP">
