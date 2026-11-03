# 최지수 | 포트폴리오

직접 만든 작업물을 모았습니다. 각 프로젝트 저장소에 실행 방법, 만든 과정, 어디까지 확인했는지를 정리해 두었습니다.

## 작업물

### MD 워크툴
온라인 MD(머천다이저)의 매출·목표·광고·프로모션·정산 업무를 한 화면에서 관리하는 브라우저 앱입니다.

- MD 업무와 마케팅·광고 두 작업 공간으로 나눠, 각자 자주 쓰는 화면부터 보이게 구성했습니다.
- 자료가 다 들어왔다고 확인한 날까지만 목표를 판정하고, 확인되지 않은 값은 0이 아니라 '판정 보류'로 둡니다.
- 보고서는 확정본으로 보관해, 나중에 자료가 바뀌어도 보고 당시 내용과 차이를 함께 보여 줍니다.
- JavaScript(빌드 없음) · IndexedDB · Chart.js · SheetJS · Node 테스트

[저장소](https://github.com/ASYNCGUY-dot/md-work-tool) · [바로 써보기](https://asyncguy-dot.github.io/md-work-tool/) (예시 데이터)

### 냉장고 한끼
냉장고에 있는 재료와 알레르기를 반영해 레시피를 추천하고, 농산물 시세(KAMIS)로 재료비를 계산하는 서비스입니다.

- 알레르기 태깅과 추천 필터를 따로 점검했습니다.
- 재료비는 찾은 시세의 부분 합계와 추정 여부를 밝히고, 다른 부위의 가격을 대신 붙이지 않습니다.
- FastAPI · React · PostgreSQL

[저장소](https://github.com/ASYNCGUY-dot/naengjango-hankki-v3) · [개발 보고서](https://github.com/ASYNCGUY-dot/naengjango-hankki-v3/blob/main/PROJECT_REPORT_V3.md)

### 계약서 돋보기
계약서 조항과 관련 법 조문을 나란히 보여 주는 도구입니다. 사진으로 찍은 계약서는 브라우저에서 글자를 읽어 냅니다(OCR).

- 표준약관과 실제 분쟁 약관을 나눠 평가하고, 관련 조문 후보를 보여 주는 도구로 범위를 정했습니다.
- 임베딩 검색 · ONNX · FastAPI · React

[저장소](https://github.com/ASYNCGUY-dot/contract-lens) · [프로젝트 개요](https://github.com/ASYNCGUY-dot/contract-lens/blob/main/docs/PORTFOLIO_OVERVIEW.md) · [실험·정정 기록](https://github.com/ASYNCGUY-dot/contract-lens/blob/main/docs/NOTES.md)

### 근거있어
건강기능식품·화장품 광고 문구를 공식 데이터와 대조해 근거영수증으로 보여 주는 엔진입니다.

- 공식 문구나 광고를 끝까지 해석하지 못하면 확인을 보류하고, 출처와 규칙 버전을 영수증에 남깁니다.
- 데이터 품질 점검 · 규칙 엔진 · 출처 추적 · 동결 평가

[저장소](https://github.com/ASYNCGUY-dot/geungeo-isseo) · [프로젝트 개요](https://github.com/ASYNCGUY-dot/geungeo-isseo/blob/main/docs/PORTFOLIO_OVERVIEW.md) · [평가·검토 근거](https://github.com/ASYNCGUY-dot/geungeo-isseo/tree/main/docs/evidence)

### Football Lens
축구 뉴스를 모아 여러 LLM으로 분석하고, 검색(RAG)으로 찾아볼 수 있게 한 대시보드입니다.

- 수집·전처리·분석·검색·화면을 나눈 파이프라인으로 만들었습니다.
- LangGraph · LangChain · ChromaDB · Streamlit

[저장소](https://github.com/ASYNCGUY-dot/football-lens-ai-agent) · [프로젝트 개요](https://github.com/ASYNCGUY-dot/football-lens-ai-agent/blob/main/docs/PORTFOLIO_OVERVIEW.md) · [파이프라인 코드](https://github.com/ASYNCGUY-dot/football-lens-ai-agent/blob/main/week2/graph.py)

### 한국어 감성분석
영화 리뷰(NSMC)로 RoBERTa 모델을 파인튜닝하고, Gradio로 바로 써 볼 수 있게 만들었습니다.

- 같은 모델에서 학습 데이터를 바꿔 가며 결과를 비교하고, 별도 테스트로 평가했습니다.
- PyTorch · Transformers · Hugging Face · Gradio

[저장소](https://github.com/ASYNCGUY-dot/Huggingface-work_korean-sentiment_nlp) · [프로젝트 개요](https://github.com/ASYNCGUY-dot/Huggingface-work_korean-sentiment_nlp/blob/main/docs/PORTFOLIO_OVERVIEW.md) · [실험 보고서](https://github.com/ASYNCGUY-dot/Huggingface-work_korean-sentiment_nlp/blob/main/REPORT.md)

---

모두 개인 프로젝트이며, 개발과 검토에 AI 도구를 함께 썼습니다. 저장소의 수치는 각 문서에 적힌 시점·자료·조건의 결과이고, 한계는 저장소마다 따로 적어 두었습니다.
