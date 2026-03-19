# public-data-eda

공공데이터를 활용한 탐색적 데이터 분석(EDA) 프로젝트 모음

## Stack

`Python` `pandas` `matplotlib` `seaborn` `scipy`

## Structure

```
public-data-eda/
├── 01_population/        # 인구통계 분석
├── 02_weather_energy/    # 기상-에너지 상관분석
├── 03_manufacturing/     # 제조업 생산지수 분석
└── utils/                # 공통 전처리 함수
```

## Projects

| # | 주제 | 데이터 출처 | 핵심 스킬 | 상태 |
|---|------|-----------|----------|------|
| 01 | 인구통계 EDA | 통계청 KOSIS | pandas, groupby, 시각화 | 예정 |
| 02 | 기상-에너지 상관분석 | 기상청 + 한전 API | merge, 상관계수, heatmap | 예정 |
| 03 | 제조업 생산지수 분석 | 통계청 광공업생산지수 | 시계열, rolling, 트렌드 | 예정 |

## How to Run

```bash
pip install pandas matplotlib seaborn scipy
jupyter notebook
```
