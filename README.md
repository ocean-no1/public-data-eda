# public-data-eda

매일 여러 사이트를 돌아다니며 유가, 환율, 금리, 주가를 확인하는 비효율을 해결하기 위해 만든 매크로 대시보드

## 해결하는 문제

> 매일 아침 네이버 금융, Investing.com, FRED, 기상청을 각각 열어서 확인하던 걸
> 하나의 대시보드에서 자동으로 볼 수 있게

## Stack

`Python` `pykrx` `pandas` `Streamlit` `Plotly` `GitHub Actions`

## Data Sources (전부 무료)

| 데이터 | 소스 | API키 |
|--------|------|-------|
| KOSPI, KOSDAQ, 섹터 지수 | pykrx (KRX 스크래핑) | 불필요 |
| 삼성전자, SK하이닉스 등 종목 시세 | pykrx | 불필요 |
| USD/KRW, USD/JPY 환율 | fawazahmed0/exchange-api | 불필요 |
| 미국 금리, VIX, CPI, 실업률 | FRED API | 무료 발급 |
| WTI, Brent, 천연가스 | EIA API | 무료 발급 |

## Structure

- `src/collect.py` — 전체 데이터 수집 스크립트
- `dashboard/app.py` — Streamlit 대시보드
- `data/` — 수집된 CSV (자동 생성)
- `config/keys.example.json` — API키 템플릿
- `.github/workflows/collect.yml` — 평일 자동 수집

## Quick Start

```bash
pip install -r requirements.txt
python src/collect.py
streamlit run dashboard/app.py
```

## Roadmap

| Phase | 내용 | 상태 |
|-------|------|------|
| 1 | 한국 주식 지수 + 환율 EDA | 진행중 |
| 2 | FRED 매크로 + EIA 유가 통합 | 예정 |
| 3 | GitHub Actions 자동 수집 | 예정 |
| 4 | Streamlit Cloud 배포 | 예정 |
