### Natural Language <-> Artificial Language

## 1. Definition
- NL: use to communicate with each other naturally
- AL: computer simulations between artificial agents, robot interactions or controlled psychological experiments with humans.

Send MSG -> Encode -> Media -> Receive MSG -> Decode (받는 수신자가 컴퓨터가 되고 이 때 일어나는 디코드 과정을 자연어처리라고 한다.)  
즉, 자연어 처리란 **자연어를 컴퓨터가 해독하고 그 의미를 이해하는 기술**을 말한다.

## 2. Application
대표적으로 **Symbolic Approach**와 **Statistic Approach**가 있다.  
예를 들어, 규칙/지식 기반 접근법에서 숫자 앞에 달러 표시가 있다면 그것은 금액을 표현하는 것을 나타내고, 오늘의 날씨가 포함된 키워드로 질문을 하면 오늘의 날씨가 포함된 키워드로 답변을 한다.  
반면 확률/통계 기반 접근법에서는 TF-IDF 메소드가 많이 사용되는데 이 때 빈도수가 많다고 할지라도 필요없는 키워드(i.g., "a", "the", "for")는 버리고 의미있는 키워드를 통해 적분법을 이용한다. 과거에는 이 두 가지 방법들이 많이 사용되었는데 요즘에는 두번째 방법과 함께 딥러닝 모델이 적용된 알고리즘이 많이 사용된다.  
한편 자연어처리에는 어마어마한 전처리 작업이 필요하다. 특수문자 제거, 조사 제거, 중복표현 제어 등 모델링을 구축하기 전 다양한 전처리 방법들이 요구된다.  

## Tokening
주어진 코퍼스(corpus)에서 토큰(token)이라 불리는 단위로 나누는 작업을 토큰화(tokenization)라고 한다. 토큰의 단위가 상황에 따라 다르지만, 보통 의미있는 단위로 토큰을 정의합니다.  
즉 자연어를 어떤 단위로 살펴볼 것인가?  

## 3. Classification
형태소 분석, 문서 분류, 개체명 인식 등 대부분의 자연어처리의 핵심은 **분류** 기술에 달려 있다.  
과거에는 사람이 직접 특징 (feature)을 파악해서 분류했으나 실제 복잡한 문제에서는 분류 대상의 특징을 사람이 파악하기 어렵다는 이유로 근래에는 이러한 특징을 컴퓨터가 스스로 찾고 (feature extraction), 스스로 분류하는 것이 기계 학습의 핵심 기술이다.  


04/01/2022

## 1. Parts of Speech and Syntactic Parsing
#### Keep in mind that:
- Making judgments on grammar is not the goal of computational linguistics [Allen, 1988]
- Checks are done to eliminate potential ambiguity that would arise if they were not used
1. Flying planes are dangerous
2. Flying planes is dangerous

#### Constituency
- Syntactic constituency is the idea that groups of words can behave as single units, or constituents.
- Part of developing a grammar involves building an inventory of the constituents in the language.
- How do words group together in English?
- What evidence do we have that these words group together (or “form constituents”)?
