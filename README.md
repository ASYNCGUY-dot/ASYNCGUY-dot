# 최지수 | AI · 공공데이터 프로젝트

공공데이터를 연결하고, 모델과 규칙의 한계를 검증하며, 사용할 수 있는 화면까지 만듭니다.

기능을 만드는 과정과 함께 **왜 그 구조를 선택했는지, 무엇을 측정했는지, 어디까지 확인했는지**를 기록합니다.
아래 프로젝트는 개인 프로젝트입니다. AI 도구를 개발·검토에 활용했으며, 평가에서 AI 라벨과 사람 검증을 구분합니다.

## 프로젝트

| 프로젝트 | 해결하려는 문제와 구현 | 확인할 수 있는 역량 |
|---|---|---|
| [냉장고 한끼](https://github.com/ASYNCGUY-dot/naengjango-hankki-v3) | 냉장고 재료·알레르기를 반영한 레시피 추천, KAMIS 시세 기반 재료비 | FastAPI · React · PostgreSQL, API 계약, 운영 오류 분석 |
| [계약서 돋보기](https://github.com/ASYNCGUY-dot/contract-lens) | 계약서 조항과 관련 법 조문을 나란히 제시, 브라우저 OCR | 임베딩 검색 · ONNX · FastAPI · React, 입력 조건별 평가 |
| [근거있어](https://github.com/ASYNCGUY-dot/geungeo-isseo) | 건강기능식품·화장품 광고를 공식 데이터와 대조하는 근거영수증 | 데이터 품질 점검, 규칙 엔진, 출처 추적, 동결 평가 |
| [Football Lens](https://github.com/ASYNCGUY-dot/football-lens-ai-agent) | 축구 뉴스 수집, 여러 LLM을 이용한 분석, RAG 검색 대시보드 | LangGraph · LangChain · ChromaDB · Streamlit |
| [한국어 감성분석](https://github.com/ASYNCGUY-dot/Huggingface-work_korean-sentiment_nlp) | NSMC 리뷰로 RoBERTa 파인튜닝, 별도 테스트 평가, Gradio 추론 | PyTorch · Transformers · Hugging Face, 데이터 비교 실험 |

## 코드를 넘어 어떤 판단을 했는가

- **냉장고 한끼:** 알레르기 태깅과 추천 필터를 따로 점검했습니다. 재료비는 찾은 시세의 부분 합계와 추정 여부를 밝히며, 다른 부위의 가격을 대신 붙이지 않습니다.
- **계약서 돋보기:** 표준약관과 실제 분쟁 약관을 나눠 평가했습니다. 쉬운 표본의 높은 점수를 전체 성능으로 소개하지 않고, 관련 조문 후보를 보여주는 도구로 범위를 제한했습니다.
- **근거있어:** 공식 문구나 광고를 끝까지 해석하지 못하면 확인을 보류합니다. 새 평가에서 효과가 확인되지 않은 규칙은 철회하고, 출처와 규칙 버전을 영수증에 남깁니다.
- **Football Lens:** 수집·전처리·분석·검색·화면을 나눈 파이프라인을 구현했습니다. 생성된 경기 전망과 실제 예측 정확도 검증은 구분합니다.
- **한국어 감성분석:** 같은 모델에서 학습 데이터를 바꾸며 결과를 비교했습니다. 높은 검증 점수만으로 성능을 설명하지 않고 별도 테스트와 도메인 한계를 함께 공개합니다.

## 빠르게 확인할 자료

| 프로젝트 | 포트폴리오 안내 | 구현·판단 근거 |
|---|---|---|
| 냉장고 한끼 | [프로젝트 개요](https://github.com/ASYNCGUY-dot/naengjango-hankki-v3/blob/main/README.md) | [개발 보고서](https://github.com/ASYNCGUY-dot/naengjango-hankki-v3/blob/main/PROJECT_REPORT_V3.md) |
| 계약서 돋보기 | [프로젝트 개요](https://github.com/ASYNCGUY-dot/contract-lens/blob/main/docs/PORTFOLIO_OVERVIEW.md) | [실험·정정 기록](https://github.com/ASYNCGUY-dot/contract-lens/blob/main/docs/NOTES.md) |
| 근거있어 | [프로젝트 개요](https://github.com/ASYNCGUY-dot/geungeo-isseo/blob/main/docs/PORTFOLIO_OVERVIEW.md) | [평가·검토 근거](https://github.com/ASYNCGUY-dot/geungeo-isseo/tree/main/docs/evidence) |
| Football Lens | [프로젝트 개요](https://github.com/ASYNCGUY-dot/football-lens-ai-agent/blob/main/docs/PORTFOLIO_OVERVIEW.md) | [파이프라인 구현](https://github.com/ASYNCGUY-dot/football-lens-ai-agent/blob/main/week2/graph.py) |
| 한국어 감성분석 | [프로젝트 개요](https://github.com/ASYNCGUY-dot/Huggingface-work_korean-sentiment_nlp/blob/main/docs/PORTFOLIO_OVERVIEW.md) | [실험 보고서](https://github.com/ASYNCGUY-dot/Huggingface-work_korean-sentiment_nlp/blob/main/REPORT.md) |

## 결과를 읽는 기준

저장소의 수치는 해당 문서에 기록된 시점·표본·조건의 결과입니다. 단위 테스트, AI가 만든 평가 라벨,
사람 검토, 실제 서비스 운영 성과를 구분합니다. 이 소개를 정리하면서 모델 재학습이나 서비스 성능 재측정은 하지 않았습니다.

- 냉장고 한끼: 배포·운영 기록이 있는 프로젝트이며 현재 동작과 무료 서버 제약은 저장소 안내를 확인해 주세요.
- 계약서 돋보기: 관련 조문을 찾는 도구이며 법률 판단을 제공하지 않습니다.
- 근거있어: 연구·개발 단계입니다. AI 라벨 평가를 사람·전문가 정확도로 해석할 수 없습니다.
- Football Lens: 개발 프로젝트입니다. 경기 예측의 실전 정확도는 이 포트폴리오에서 입증하지 않습니다.
- 한국어 감성분석: 영화 리뷰 도메인의 실험이며 다른 도메인 성능은 별도로 검증해야 합니다.

공개 영역에는 프로젝트별 코드·실행 방법·판단 근거를, 비공개 영역에는 내부 계획과 개발 메모를 관리합니다.
