# CEO Twitter Market Impact

CEO 트위터 시장 영향 프로젝트의 기본 연구 구조와 재현 가능한 baseline 산출물을 담은 저장소입니다.

**핵심 연구 질문**

> CEO의 공개 발언 톤은 이벤트 당일과 직후 주가 반응에 어떤 차이를 만드는가?

## 작업 기준 문서

- `AGENTS.md`: 저장소 작업 기준과 품질 기준
- `SOURCE.md`: KAIST-DFMBA 참고 경로와 프로젝트별 컨텐츠 재구성 기준

## 저장소 구조

```text
ceo-twitter-market-impact/
├── src/                         # baseline 계산 로직과 실행 엔트리포인트
├── data/sample/                 # 합성 샘플 입력 데이터
├── docs/                        # 방법론과 해석 기준
├── notebooks/                   # 실행 흐름을 보여주는 최소 노트북
├── outputs/tables/              # 재현 가능한 결과 CSV
├── presentation/                # 발표/보고서 초안
└── references/                  # 재작성 개념 노트와 참고문헌 메모
```

## 빠른 시작

```bash
python -m src.run_baseline
```

실행 결과는 `outputs/tables/baseline_results.csv`에 저장됩니다.

## 구현 범위

- 이벤트 윈도우 -1, 0, +1일의 주식수익률에서 시장수익률을 차감해 abnormal return을 만든다.
- CAR를 톤별로 비교해 이벤트 영향의 방향성과 지속성을 확인한다.
- 이벤트와 수익률은 이벤트 스터디 계산 흐름을 설명하는 합성 예시다.

## 주요 파일

- `src/event_study_baseline.py`: CEO 발언 이벤트 주변의 abnormal return과 누적반응을 요약한다.
- `data/sample/ceo_event_returns.csv`: baseline 실행용 합성 입력값
- `docs/methodology.md`: 계산 절차, 입력/출력 정의, 해석상 주의점
- `outputs/tables/baseline_results.csv`: 현재 baseline 산출물

## 다음 확장 방향

- 실제 공개 데이터 또는 별도 수집 데이터 연결
- notebook 기반 탐색 분석 추가
- 차트와 표를 포함한 최종 보고서 작성
- 모델 검증, 민감도 분석, 비용/리스크 가정 보강
