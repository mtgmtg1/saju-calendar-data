# 사주 만세력 데이터 1900~2100 (Saju calendar data)

[명리연구소](https://saju.teamcat.app/data)의 만세력이 계산하는 표 세 가지를 CSV 로 공개합니다.
사이트 화면과 같은 계산 함수에서 만든 값이며, 원본 배포 주소는 <https://saju.teamcat.app/data> 입니다.

| 파일 | 내용 | 행 수 |
| --- | --- | --- |
| [`data/solar-terms-1900-2100.csv`](data/solar-terms-1900-2100.csv) | 24절기 절입 시각(분 단위) | 4,824 |
| [`data/daily-ganji-1900-2100.csv`](data/daily-ganji-1900-2100.csv) | 날짜별 일진(일주 간지)·음력·절기 | 73,414 |
| [`data/zodiac-boundary-1900-2100.csv`](data/zodiac-boundary-1900-2100.csv) | 연도별 띠 경계 — 입춘 절입 순간, 음력 설날, 두 기준이 갈리는 날짜 구간, 윤달 | 201 |

## 출처와 계산 기준

- 절입 시각은 분 단위 천문 계산값입니다.
- 음력은 2049년까지 한국천문연구원(KASI) 음양력 자료, 2050년 이후는 천문 계산값입니다.
- `kst` 열은 UTC+9 로 환산한 표기입니다. 한국이 다른 표준시(UTC+8:30, 일광절약시간)를 쓰던 시기의
  실제 시계는 연도별 페이지(예: <https://saju.teamcat.app/free-manse/year/1988>)에 있습니다.
- 계산 기준 전체: <https://saju.teamcat.app/encyclopedia/method>

## 열 설명

**solar-terms** — `year` 연도 · `name`/`hanja` 절기 이름 · `kind` section=절(節), mid=중기(中氣) ·
`utc` 절입 순간(ISO 8601) · `kst` 한국 표준시 표기 · `month_branch` 그 절이 여는 명리월의 지지

**daily-ganji** — `date` 양력 날짜 · `ganji`/`ganji_hanja` 일진 · `lunar` 음력 날짜 · `lunar_leap` 윤달이면 1 ·
`term` 그날 드는 절기

**zodiac-boundary** — `year` · `ganji` 그해 연주 · `zodiac` 그해 띠 · `prev_zodiac` 입춘 전 출생자의 띠 ·
`ipchun_kst` 입춘 절입 순간 · `seollal` 음력 1월 1일의 양력 날짜 · `split_from`/`split_until` 두 기준의 띠가
갈리는 구간(끝 날짜 전까지) · `ipchun_first` 입춘이 설날보다 먼저면 1 · `leap_month` 그 음력 해의 윤달

파일은 UTF-8(BOM 포함)이라 엑셀에서 한글이 그대로 열립니다.

## 라이선스

[CC BY 4.0](LICENSE). 출처를 밝히면 상업적 이용을 포함해 자유롭게 쓸 수 있습니다.

> 출처: 명리연구소 만세력 데이터, https://saju.teamcat.app/data

---

## English

Three tables computed by the Korean saju (Four Pillars) calendar engine behind
[saju.teamcat.app](https://saju.teamcat.app/data), covering 1900–2100:
solar-term (jieqi) entry times to the minute, the sexagenary day stem-branch with the lunar date for every day,
and the yearly zodiac boundary (Ipchun instant vs. Lunar New Year, the date range where the two conventions
disagree, and the leap month). Solar terms are astronomical calculations; lunar dates follow the Korea Astronomy
and Space Science Institute (KASI) tables through 2049 and are calculated afterwards. Licensed CC BY 4.0.
