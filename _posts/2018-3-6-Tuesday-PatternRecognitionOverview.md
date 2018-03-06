---
title: Patternn Recognition Overview
author: EzoBear
layout: post
category: PatternRecognition
---
본 포스팅은 Index와 같이 구성되며, Pattern Recognition의 전체적인 개념과 흐름에 대한 개요만을 다룹니다. 세부적인 요소들은 차후 따로 포스팅 예정입니다.
<h2>Index</h2>

<a href="url">0.History</a><br>
<a href="url">1.Definition</a><br>
<a href="url">2.Pattern</a><br>
<a href="url">3.Process</a><br>
<a href="url">4.Kinds</a><br>
<a href="url">5.Classifier</a><br>
<a href="url">6.System Evaluation</a><br>
<a href="url">7.Approach Method</a><br>
<a href="url">8.Example</a><br>
<a href="url">9.Applications</a><br>
<h2></h2>

<h2>History</h2><br>
<a>
패턴인식은 '컴퓨터도 인간과 같이 생각할 수 있을까?' 라는 의문에서부터 시작됩니다. 이러한 물음에 해답을 찾기 위해 수많은 연구자들이 인간의 지능을 연구하고, 이를 기계에 구현하려고 노력해왔습니다. 여러분이 잘 알고있는 인공지능이라는 형태로 말입니다. 그렇기 때문에 인공지능은 사람이 생각하고 행동하는 것에 초점을 맞춰 잘 추상화 되어있습니다. 이렇게 추상화된 인공지능의 처리과정을 지능적 처리라고하며, 크게 인식, 해석, 행동의 과정으로 나누어집니다.
인식은 센싱 인터페이스를 통해 외부 자극 신호를 받아들이는 과정입니다.
해석은 이렇게 수집한 센싱 데이터들을 분석하여 객체 혹은 상황을 인식하고, 그 결과에 따라 선택적 판단을 하는 과정입니다.
행동은 이러한 선택적 판단 결과에 따라 문제를 해결 혹은 작업을 수행하는 과정을 뜻합니다.
패턴인식은 이러한 인공지능의 한 부분으로써 지능적 처리과정 중 해석 부분에서 수집한 데이터를 분석하고 객체 혹은 상황을 인식하는 과정을 말합니다.
즉, 패턴인식은 공학적 접근법을 이용하여 인공지능의 실제 구현 문제인 감지된 대상을 인식하는 문제를 주로 다루는 방법입니다.
</a>

<h2>Definition</h2><br>
0장을 통해 패턴인식이 무엇인지에 대해 알게되었습니다.그러나 너무 추상적입니다. 그래서 본 장에서는 여러 대가들의 패턴인식에 대한 정의를 살펴보고, 생각해보는 시간을 갖겠습니다[1].

1.R. Schalkoff et al, "Pattern Recognition. Statistical, Structural, and Neural Approaches"에서는 "The science that concerns the description or classification(recognition) of measurements" 라 정의했습니다. 이를 통해 뭔지는 모르겠지만 무언가의 척도의 설명이나 분류와 관련된 학문이라는 것을 알 수 있습니다. 

2.Samuel F.B Morse는 "Pattern Recognition is concerned with answering the question "What is this?" 라고 패턴인식에 대해 정의했습니다. 이는 저희가 정의했던것보다 더 추상적이지만 하고자 하는 목적은 명확합니다. 이를 좀 더 명확하게 표현한 정의들을 살펴보겠습니다.

4.3."The process of giving names w to observations x"(J. Schuermnn)
4."The assignment of a physical object or event to one of several prespecified categories"(Duda, Hart, Stork)
5."Given some examples of complex signals and the correct descions for them, make decisions automatically for a stream of future examples"(B. Ripley,1996)
6."A problem of estimating density function in a high-dimensional space and dividing the space into the regions of categories or classes"(Keinosuke Fukunalga)

작성 중
Reference
[1]한학용, 패턴인식 개론 : Matlab 실습을 통한 입체적 학습, pp 27



