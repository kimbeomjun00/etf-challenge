# 머니투데이 ETF 투자왕 프로젝트

## 프로젝트 개요

이 저장소는 머니투데이 ETF 투자왕 참가를 위해 작성한 **오전 애널리스트 리포트, 장 마감 리뷰, 투자 로그, 운용 매뉴얼**을 보관합니다.

전략은 **거시 환경을 반영한 재량적 ETF 배분·섹터 로테이션과 전술적 헤지**로 분류하는 것이 가장 정확합니다. 경제지표, 중앙은행 결정, 기업 뉴스 등은 포지션의 촉매와 판단 근거로 활용하지만, 이 저장소의 전략을 기관투자 업계에서 말하는 기업 특수상황형 **이벤트 드리븐(event-driven)** 전략으로 분류하지는 않습니다.

또한 사전에 정한 손절·포지션 한도·일일 손실 한도는 규칙 기반이지만, 종목 선택과 진입 판단에는 재량이 포함됩니다. 따라서 완전한 시스템 매매나 알고리즘 전략으로 표현하지 않습니다.

## 전략 구조

- 시장·거시 환경 점검
- 주도 섹터와 상대강도 판단
- 핵심 ETF 포지션 선정
- 필요 시 인버스 ETF를 이용한 전술적 헤지
- 사전 손절선, 포지션 한도, 손익비 점검
- 장 마감 후 성과와 판단 과정 복기

핵심 포지션과 인버스 헤지를 함께 보유하더라도 노출이 완전히 상쇄되지 않으면 **시장중립(market-neutral)**이 아닙니다. 방향성 노출이 줄어든 롱 포트폴리오 또는 부분 헤지 포지션으로 설명하는 것이 적절합니다.

## 리스크 관리 원칙

운용 매뉴얼의 주요 기준은 다음과 같습니다.

- 기준 운용자금: **10억원**
- 개별 포지션 기본 손절: **-5%**
- 최소 기대 손익비: **1:1.5**, 권장 **1:2 이상**
- 일반 / Strong / A+ 등급별 포지션 한도 운영
- 총 투입 한도와 일일 손실 중단 기준 운영
- 같은 테마나 위험요인에 대한 중복 노출 점검

여기서 `Strong`, `A+`는 운용자가 정의한 **재량적 셋업 등급**입니다. 통계적으로 보정된 성공확률이나 신용등급을 의미하지 않습니다.

## 용어 사용 원칙

### 1. 투입금액과 시장노출

- **투입금액(capital deployed):** 실제 매수에 사용한 금액
- **유효 노출(effective exposure):** ETF의 목표 배율을 반영한 명목상 방향 노출
- **총 유효노출(gross effective exposure):** 방향과 무관하게 유효 노출의 절댓값을 합산한 값
- **순 방향노출(net directional exposure):** 롱 유효 노출에서 숏 유효 노출을 차감한 값

예를 들어 일반 ETF를 1억5천만원 매수하고 `-2x` 인버스 ETF를 3천만원 매수했다면:

- 투입금액: **1억8천만원**
- 인버스의 명목상 유효 숏 노출: **약 6천만원**
- 총 유효노출: **약 2억1천만원**
- 순 방향노출: **약 +9천만원**

이는 목표 배율을 단순 적용한 설명입니다. 실제 민감도는 기초지수 차이, 베타, 일일 재조정, 추적오차, 비용에 따라 달라집니다.

### 2. 헤지비율

`3천만원 ÷ 1억5천만원 = 20%`는 **투입금액 기준 헤지 배분 비율**입니다. `-2x` 배율까지 반영한 명목상 헤지비율은 약 **40%**입니다. 문서에서는 두 기준을 구분해 표기합니다.

### 3. 상대가치, 차익거래, 알파

- 두 ETF의 상대적 성과 차이를 노리는 포지션은 일반적으로 **상대가치(relative-value) 거래**입니다.
- 무위험 또는 기계적으로 수렴이 보장되지 않는다면 **차익거래(arbitrage)**라고 부르지 않습니다.
- 벤치마크와 위험요인을 조정한 초과수익을 계산하지 않았다면 **알파(alpha)** 대신 **상대성과** 또는 **초과수익**이라고 표현합니다.

### 4. 리스크 예산

포지션 한도와 손절 규칙을 이용한 **리스크 예산(risk budget)**은 사용할 수 있는 손실 허용액을 뜻합니다. 변동성 기여도를 맞추는 **리스크 패리티**나 목표 변동성을 유지하는 **변동성 타기팅**과는 다른 개념입니다.

## 저장소 구성

자료는 `머니투데이 ETF 투자왕/` 폴더에 있습니다.

- `ETF투자왕_오전_애널리스트리포트_YYYY-MM-DD.pdf`: 개장 전 시장·전략 리포트
- `ETF투자왕_장마감리포트_YYYY-MM-DD.pdf`: 장 마감 후 리뷰
- `ETF투자왕_투자로그_YYYY-MM-DD.xlsx`: 거래 및 운용 기록
- `ETF투자왕_투자운영매뉴얼_v1.2.pdf`: 포지션·손절·등급별 운용 기준
- `거래가능종목.xlsx`: 대회 거래 가능 ETF 목록
- `ETF투자왕 HTS 매뉴얼 .pdf`: 대회 HTS 사용 안내

일자별 파일은 거래일·작성 시점에 따라 일부 비어 있을 수 있으며, 리포트는 당시 이용 가능했던 정보와 시나리오를 기록한 자료입니다.

## 해석 시 유의사항

- 리포트의 시나리오는 확정적 전망이 아니라 조건부 대응 계획입니다.
- 인버스·레버리지 ETF는 일일 수익률 배수를 목표로 하므로 장기 누적성과가 단순 배수와 달라질 수 있습니다.
- 표시된 가격·노출·손익은 각 파일의 기준시점과 계산 기준을 함께 확인해야 합니다.
- 본 저장소는 대회 기록과 포트폴리오 목적의 자료이며 투자 권유가 아닙니다.

---

## English summary

This repository archives pre-market analyst notes, end-of-day reviews, trade logs, and operating rules prepared for the MoneyToday ETF Investment Challenge.

The approach is best described as **discretionary, macro-aware ETF allocation and sector rotation with tactical hedging**. Macro releases and company news are treated as catalysts and decision inputs; the strategy is not presented as corporate-special-situations event-driven investing, a fully systematic strategy, or a market-neutral portfolio.

Terminology in this repository distinguishes capital deployed from leverage-adjusted exposure, capital-allocation hedge ratios from effective hedge ratios, relative-value trades from arbitrage, and unadjusted relative performance from alpha.

> These materials document a competition process for educational and portfolio purposes. They are not investment advice.
