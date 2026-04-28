# 발표 초안

## 1. 문제 정의

CEO의 공개 발언 톤은 이벤트 당일과 직후 주가 반응에 어떤 차이를 만드는가?

## 2. 데이터와 가정

- 합성 샘플 데이터: `data/sample/ceo_event_returns.csv`
- 재현 가능한 baseline 실행을 우선 구성

## 3. 방법

CEO 발언 이벤트 주변의 abnormal return과 누적반응을 요약한다.

## 4. 현재 산출물

- 실행 스크립트: `python -m src.run_baseline`
- 결과 표: `outputs/tables/baseline_results.csv`

## 5. 후속 작업

- 실제 데이터 연결
- 민감도 분석
- 차트/보고서 산출
- 프로젝트별 상세 검증
