---
layout: page
title: Parser
description: an arithmetic expression parser written in C++
img: /assets/parser/grammar.png
importance: 1
category: course
---

[👁 on Github](https://github.com/yiren-lu/bachelor-cs/tree/master/parser)

An LL(1) along with one LR(1) parser written C++, accepting the following grammar(a grammar generating basic arithmetic formula):

$$
\begin{aligned}
E\to & E+T | E-T | T\\
T\to & T * F | T / F | F\\
F\to & (E) |\text{num}
\end{aligned}
$$

which is rewritten into an equivalent instance to avoid left recursions(which cannot be dealt by LL(1) parsing but ok for LR(1) parsing)

$$
\begin{aligned}
E \to& T E'\\
E' \to& + T E' | - T E' | \varepsilon\\
T \to& F T'\\
T' \to& * F T' | / F T' | \varepsilon\\
F\to& ( E ) | \text{num}
\end{aligned}
$$

I implemented all subprograms needed to implement LL(1) parsing and LR(1) parsing, such as solving $$\varepsilon$$-set, FOLLOW-set, etc. You can refer to the following document(Chinese) for details.

<object data="/assets/parser/document.parser.pdf" width="100%" height="1000" type='application/pdf'/>
