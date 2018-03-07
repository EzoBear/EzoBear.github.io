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

2.Samuel F.B Morse는 "Pattern Recognition is concerned with answering the question "What is this?" 라고 패턴인식에 대해 정의했습니다. 이는 저희가 정의했던것보다 더 추상적이지만 하고자 하는 목적은 명확합니다.

3."A problem of estimating density function in a high-dimensional space and dividing the space into the regions of categories or classes"(Keinosuke Fukunalga)
(다차원 공간 내에서 밀도함수를 추정하고, 공간을 카테고리 혹은 클래스 영역으로 분리하는 문제)
이를 좀더 수학적으로 표현해보면 3번과 같이 표현할 수 있습니다.

이를 의미론 적으로 정의한 정의를 몇가지 살펴보면
4."The process of giving names w to observations x"(J. Schuermnn)
5."The assignment of a physical object or event to one of several prespecified categories"(Duda, Hart, Stork)
6."Given some examples of complex signals and the correct descions for them, make decisions automatically for a stream of future examples"(B. Ripley,1996)
4,5.6을 잘 종합해보면 관측값 x에 이름 w를 부여한뒤,
물리적 객체 혹은 사건에 이미 정해진 몇 카테고리인 w로 할당하고,
미래에 표본들에 대하여 자동적으로 결정을 내리하게 하는 것.
이라고 생각할 수 있습니다.

즉, 패턴인식이란 관측값 x에 이름w를 부여한 뒤, 물리적 객체 혹은 사건에 이미 정해진 몇 카테고리인 w로 할당하고, 미래에 표본들이 생겼을때, 이를 자동으로 분류하는 것 이라고 말할 수 있습니다. 이는 다차원 공간 내에서 밀도함수를 추정하는 것으로 이루어지는 것이고요.

살펴보듯 정의는 다양하게 이루어져 있지만 결국 패턴을 찾아내고, 패턴을 분류하여 패턴에 이름 붙이는 것이 가장 중요한 키 포인트입니다.

그렇다면 패턴이라는 것은 무엇일까요?
<a>
<h2>Pattern</h2><br>
패턴은 여러분도 잘 알듯 일정하게 반복되는 특징의 집합 정도로 표현하면 아마 큰 무리가 없을겁니다. 그렇다면 특징이란 무엇일까요? 특징은 다른 것과 구분되는 점이지요. 즉, 패턴인식에서는 분류할 대상이 되는 객체를 구분할 수 있는 aspect, quality,feature 쯤 될것입니다. 예를들어 은행잎인지, 단풍잎인지 를 구분한다하면, 노란색이면 은행나무, 붉은색이면 단풍나무일겁니다. 이렇듯 색깔과 같은 상징적인 것이 될 수 있습니다. 또 다른 예시를 들어보면 돌맹이와 바위를 구분한다고 하면, 높이,면적,무게와 같은 수치적인 것들이 될수도 있겠네요.또다른 예시를 들어보겠습니다.
참치와 고등어를 구분한다고 치면, 참치는 크고, 고등어는 작습니다.(크기,길이 넓이) 다른 특징으로는 고등어는 등이 푸르네요, 참치는 그렇지 않네요(색깔).
이렇듯 상직적인 특징과 수치적인 특징은 복합적으로도 사용될 수 있습니다.


Reference
[1]한학용, 패턴인식 개론 : Matlab 실습을 통한 입체적 학습, pp 27



