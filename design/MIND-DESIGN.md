---
version: alpha
name: MIND-IoT-Platform-design-system
description: A control-surface design system for MIN.D IoT integration platforms. Dark-first because operators read these screens at night and on wall displays; device state is the only thing allowed to use color, so a single glance separates healthy from failing. Navy (#1B2B41) carries structure, one brand blue (#3A88B4) carries every interactive affordance, and semantic state colors are reserved exclusively for device status — never for decoration. Pretendard throughout, 4pt corners, 44px minimum touch targets, and numeric readouts in tabular figures so live values never reflow.

colors:
  primary: "#3A88B4"
  primary-strong: "#2F7399"
  primary-hover: "#2F7399"
  primary-pressed: "#25607F"
  primary-subtle: "#66B2E0"
  navy: "#1B2B41"
  navy-raised: "#22354F"
  navy-sunken: "#15222F"
  ink: "#1B2B41"
  body: "#333333"
  body-muted: "#6B7280"
  body-on-dark: "#FFFFFF"
  body-muted-on-dark: "#9AA8BC"
  canvas: "#FFFFFF"
  canvas-soft: "#F6F7F8"
  canvas-dark: "#101B26"
  surface: "#FFFFFF"
  surface-dark: "#1B2B41"
  surface-raised-dark: "#22354F"
  hairline: "#D5D2CA"
  hairline-strong: "#1B2B41"
  hairline-on-dark: "#2C3F58"
  state-online: "#1F9D72"
  state-online-ink: "#15795A"
  state-online-bg: "#E7F5EF"
  state-online-on-dark: "#3FC397"
  state-warning: "#C98A14"
  state-warning-ink: "#8A5D00"
  state-warning-bg: "#FBF3E0"
  state-warning-on-dark: "#E3A93A"
  state-error: "#C5433B"
  state-error-ink: "#A62F28"
  state-error-bg: "#FBEAE9"
  state-error-on-dark: "#F0736A"
  state-offline: "#8A94A6"
  state-offline-ink: "#5A6373"
  state-offline-bg: "#EEF0F3"
  state-offline-on-dark: "#9AA8BC"
  state-connecting: "#3A88B4"
  chip: "#D5D2CA"
  on-primary: "#FFFFFF"
  on-navy: "#FFFFFF"
  focus-ring: "#66B2E0"

typography:
  display:
    fontFamily: "Pretendard, -apple-system, BlinkMacSystemFont, system-ui, sans-serif"
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: -0.6px
  page-title:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.33
    letterSpacing: -0.4px
  section-title:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 18px
    fontWeight: 600
    lineHeight: 1.44
    letterSpacing: -0.2px
  card-title:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: -0.2px
  body:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 15px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: -0.1px
  body-strong:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 15px
    fontWeight: 600
    lineHeight: 1.6
    letterSpacing: -0.1px
  caption:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.54
    letterSpacing: 0
  label:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 12px
    fontWeight: 600
    lineHeight: 1.33
    letterSpacing: 0.2px
  metric-hero:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 44px
    fontWeight: 300
    lineHeight: 1.1
    letterSpacing: -1px
    fontVariantNumeric: tabular-nums
  metric:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 28px
    fontWeight: 300
    lineHeight: 1.2
    letterSpacing: -0.5px
    fontVariantNumeric: tabular-nums
  metric-unit:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0
  ordinal:
    fontFamily: "Pretendard, -apple-system, system-ui, sans-serif"
    fontSize: 24px
    fontWeight: 200
    lineHeight: 1.0
    letterSpacing: 0
  mono:
    fontFamily: "JetBrains Mono, SFMono-Regular, Menlo, monospace"
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0

rounded:
  none: 0px
  sm: 4px
  md: 4px
  lg: 8px
  xl: 12px
  pill: 9999px
  full: 9999px

spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  section: 64px

components:
  button-primary:
    backgroundColor: "{colors.primary-strong}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body-strong}"
    rounded: "{rounded.md}"
    padding: 12px 20px
    height: 44px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.md}"
  button-secondary:
    backgroundColor: transparent
    textColor: "{colors.primary-strong}"
    borderColor: "{colors.primary}"
    borderWidth: 1px
    typography: "{typography.body-strong}"
    rounded: "{rounded.md}"
    padding: 12px 20px
    height: 44px
  button-quiet:
    backgroundColor: transparent
    textColor: "{colors.body-muted}"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: 12px 16px
    height: 44px
  button-destructive:
    backgroundColor: "{colors.state-error}"
    textColor: "{colors.on-primary}"
    typography: "{typography.body-strong}"
    rounded: "{rounded.md}"
    padding: 12px 20px
    height: 44px
  device-card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    borderColor: "{colors.hairline}"
    borderWidth: 1px
    typography: "{typography.card-title}"
    rounded: "{rounded.lg}"
    padding: 20px
    minHeight: 132px
  device-card-active:
    backgroundColor: "{colors.navy}"
    textColor: "{colors.on-navy}"
    borderColor: "{colors.navy}"
    borderWidth: 1px
    rounded: "{rounded.lg}"
    padding: 20px
  device-card-dark:
    backgroundColor: "{colors.surface-raised-dark}"
    textColor: "{colors.body-on-dark}"
    borderColor: "{colors.hairline-on-dark}"
    borderWidth: 1px
    rounded: "{rounded.lg}"
    padding: 20px
  device-card-alarm:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    borderColor: "{colors.state-error}"
    borderWidth: 1px
    rounded: "{rounded.lg}"
    padding: 20px
  status-badge-online:
    backgroundColor: "{colors.state-online-bg}"
    textColor: "{colors.state-online-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: 4px 10px
    height: 24px
  status-badge-warning:
    backgroundColor: "{colors.state-warning-bg}"
    textColor: "{colors.state-warning-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: 4px 10px
    height: 24px
  status-badge-error:
    backgroundColor: "{colors.state-error-bg}"
    textColor: "{colors.state-error-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: 4px 10px
    height: 24px
  status-badge-offline:
    backgroundColor: "{colors.state-offline-bg}"
    textColor: "{colors.state-offline-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: 4px 10px
    height: 24px
  status-dot:
    size: 8px
    rounded: "{rounded.full}"
  toggle-track-on:
    backgroundColor: "{colors.primary-strong}"
    rounded: "{rounded.pill}"
    width: 52px
    height: 32px
  toggle-track-off:
    backgroundColor: "{colors.state-offline}"
    rounded: "{rounded.pill}"
    width: 52px
    height: 32px
  toggle-thumb:
    backgroundColor: "{colors.canvas}"
    rounded: "{rounded.full}"
    size: 28px
  metric-tile:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.ink}"
    typography: "{typography.metric}"
    rounded: "{rounded.lg}"
    padding: 20px
    minHeight: 112px
  metric-tile-dark:
    backgroundColor: "{colors.surface-raised-dark}"
    textColor: "{colors.body-on-dark}"
    typography: "{typography.metric}"
    rounded: "{rounded.lg}"
    padding: 20px
  accent-rail-card:
    backgroundColor: transparent
    textColor: "{colors.ink}"
    borderLeftColor: "{colors.primary}"
    borderLeftWidth: 2px
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: 12px 0 12px 16px
  input-text:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    borderColor: "{colors.hairline}"
    borderWidth: 1px
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: 12px 14px
    height: 44px
  input-focus:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    borderColor: "{colors.primary}"
    borderWidth: 1px
    rounded: "{rounded.md}"
  chip:
    backgroundColor: "{colors.chip}"
    textColor: "{colors.ink}"
    typography: "{typography.caption}"
    rounded: "{rounded.md}"
    padding: 6px 12px
    height: 32px
  chip-selected:
    backgroundColor: "{colors.navy}"
    textColor: "{colors.on-navy}"
    typography: "{typography.caption}"
    rounded: "{rounded.md}"
    padding: 6px 12px
    height: 32px
  top-bar:
    backgroundColor: "{colors.navy}"
    textColor: "{colors.on-navy}"
    typography: "{typography.body-strong}"
    height: 56px
    padding: 0 24px
  side-nav:
    backgroundColor: "{colors.navy-sunken}"
    textColor: "{colors.body-muted-on-dark}"
    typography: "{typography.body}"
    width: 240px
    padding: 16px 12px
  side-nav-item-active:
    backgroundColor: "{colors.navy-raised}"
    textColor: "{colors.body-on-dark}"
    borderLeftColor: "{colors.primary}"
    borderLeftWidth: 2px
    rounded: "{rounded.md}"
    height: 44px
    padding: 0 14px
  table-header:
    backgroundColor: transparent
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    borderBottomColor: "{colors.hairline-strong}"
    borderBottomWidth: 1px
    height: 44px
  table-row:
    backgroundColor: transparent
    textColor: "{colors.body}"
    typography: "{typography.body}"
    borderBottomColor: "{colors.hairline}"
    borderBottomWidth: 1px
    height: 52px
  toast-alarm:
    backgroundColor: "{colors.navy}"
    textColor: "{colors.on-navy}"
    borderLeftColor: "{colors.state-error}"
    borderLeftWidth: 3px
    typography: "{typography.body}"
    rounded: "{rounded.lg}"
    padding: 16px 20px
  empty-state:
    backgroundColor: "{colors.canvas-soft}"
    textColor: "{colors.body-muted}"
    typography: "{typography.body}"
    rounded: "{rounded.lg}"
    padding: 48px 24px
---

# MIN.D IoT Platform — DESIGN.md

마인드(MIN.D)의 IoT 연동 플랫폼 화면을 위한 디자인 시스템 명세.
AI 에이전트(Claude Code / Claude Design / Cursor / Figma Make)가 이 파일을 읽고
일관된 UI를 생성하도록 작성됐다. 제안서 PPT 규격(`ppt-design-system-v2`)과
같은 토큰을 화면용으로 옮긴 것이므로, **제안서와 실제 제품이 같은 얼굴**을 갖는다.

## Overview

이 시스템이 다루는 화면은 "보는 화면"이 아니라 **조작하는 화면**이다.
기기를 켜고 끄고, 값을 바꾸고, 고장을 찾는다. 그래서 세 가지가 다른 시스템과 다르다.

1. **색은 상태의 언어다.** 장식에 색을 쓰지 않는다. 화면에서 초록·노랑·빨강이 보이면
   그건 반드시 기기 상태다. 브랜드 블루(`#3A88B4`)는 "누를 수 있는 것"에만 쓴다.
2. **다크가 기본이다.** 야간 관제, 벽면 디스플레이, 현장 태블릿이 주 환경이다.
   라이트 모드는 관리자 웹·리포트용으로 함께 제공하되, 다크에서 먼저 검증한다.
3. **숫자는 흔들리지 않는다.** 실시간 값은 tabular figures로 고정폭을 쓴다.
   `23.4°C` → `9.8°C`로 바뀔 때 레이아웃이 밀리면 안 된다.

## Colors

### Brand & Interactive
| 토큰 | HEX | 용도 |
|---|---|---|
| `primary` | `#3A88B4` | 브랜드 식별색 — 액센트 레일, 테두리, 아이콘, 활성 인디케이터, 차트 |
| `primary-strong` | `#2F7399` | **흰 글자가 올라가는 면**(기본 버튼, 토글 ON)과 흰 배경 위 링크 텍스트 |
| `primary-hover` | `#2F7399` | 호버 |
| `primary-pressed` | `#25607F` | 눌림 |
| `primary-subtle` | `#66B2E0` | 2차 위계 면, 포커스 링, 차트 보조 계열 |
| `navy` | `#1B2B41` | 상단 바, 사이드 내비, 활성 카드, 구조적 면 |

브랜드 블루는 **하나로 통일**한다. 위계는 색을 늘려서가 아니라 진하기 흐름으로 만든다:
`#D5D2CA → #66B2E0 → #3A88B4 → #1B2B41`.

> **왜 `primary-strong`이 따로 있나.** 브랜드 블루 `#3A88B4` 위의 흰 글자는 대비 3.92:1로
> WCAG AA(4.5:1)에 미달한다. 그래서 **색면으로 쓸 때는 `#3A88B4`, 그 위에 흰 글자를
> 얹을 때는 `#2F7399`(5.21:1)** 로 한 단계 내린다. 나란히 두면 구분이 거의 안 되므로
> 브랜드 인상은 유지되고 접근성만 확보된다. 링크 텍스트도 같은 이유로 `#2F7399`를 쓴다.

### Device State — 이 색들은 상태 전용이다
| 토큰 | HEX | 의미 |
|---|---|---|
| `state-online` | `#1F9D72` | 정상 연결·동작 중 |
| `state-warning` | `#C98A14` | 임계치 근접, 점검 필요 |
| `state-error` | `#C5433B` | 고장, 통신 실패, 알람 |
| `state-offline` | `#8A94A6` | 전원 꺼짐·미연결 (무채색이어야 한다 — "문제"가 아니라 "없음") |
| `state-connecting` | `#3A88B4` | 페어링·연결 시도 중 (브랜드 블루 = 진행 중) |

각 상태는 **3종 세트**로 쓴다. 용도를 섞으면 대비가 깨진다.

| 용도 | 토큰 | 정상 / 점검 / 오류 / 오프라인 |
|---|---|---|
| 점·아이콘·테두리 (비텍스트) | `state-*` | `#1F9D72` / `#C98A14` / `#C5433B` / `#8A94A6` |
| **밝은 배지 위 글자** | `state-*-ink` | `#15795A` / `#8A5D00` / `#A62F28` / `#5A6373` |
| **다크 배경 위 글자** | `state-*-on-dark` | `#3FC397` / `#E3A93A` / `#F0736A` / `#9AA8BC` |

배지 라벨은 12px/600 — WCAG 기준 '큰 글자'가 아니므로 4.5:1이 필요하다.
본색(`state-*`)을 그대로 글자에 쓰면 2.6~4.2:1로 미달한다. 반드시 `-ink`를 쓴다.

**색만으로 상태를 전달하지 않는다.** 모든 상태 배지는 점(dot) + 텍스트 라벨을 함께 갖는다.
색각 이상 사용자와 흑백 출력 리포트에서 상태가 사라지면 안 된다.

### Surface
| 토큰 | HEX | 용도 |
|---|---|---|
| `canvas` / `canvas-soft` | `#FFFFFF` / `#F6F7F8` | 라이트 배경 / 함몰 영역 |
| `canvas-dark` | `#101B26` | 다크 배경 (네이비보다 어둡다 — 카드가 떠 보이게) |
| `surface-dark` | `#1B2B41` | 다크 카드 면 |
| `surface-raised-dark` | `#22354F` | 다크 상위 레이어 |
| `hairline` | `#D5D2CA` | 라이트 구분선 1px |
| `hairline-on-dark` | `#2C3F58` | 다크 구분선 1px |

## Typography

전 구간 **Pretendard**. `Pretendard Variable`이 있으면 우선 사용한다.
한글·영문·숫자가 한 폰트 안에서 해결되므로 폰트 스택을 섞지 않는다.

| 역할 | 크기 / 굵기 | 비고 |
|---|---|---|
| `display` | 32 / 600 | 대시보드 최상단 |
| `page-title` | 24 / 600 | 페이지 제목 |
| `section-title` | 18 / 600 | 섹션 |
| `card-title` | 16 / 600 | 카드 제목, 기기명 |
| `body` | 15 / 400 | 본문 — **하한** |
| `caption` | 13 / 400 | 보조 설명, 타임스탬프 |
| `label` | 12 / 600 | 배지, 표 헤더. letter-spacing +0.2 |
| `metric-hero` / `metric` | 44 / 200·300, 28 / 300 | 실시간 수치. **tabular-nums 필수** |
| `ordinal` | 24 / 200 | 순번(01, 02) — 얇게 |
| `mono` | 13 / 400 | 기기 ID, MAC, 페이로드 |

원칙: 크기 단계는 위 목록이 전부다. 새 크기를 만들지 말고 굵기와 색으로 위계를 만든다.
본문 15px 미만은 쓰지 않는다(표 셀 13px만 예외).

## Layout

### Spacing
4의 배수: `4 / 8 / 12 / 16 / 24 / 32 / 48 / 64`.
카드 내부 패딩 20, 카드 사이 간격 16, 섹션 사이 간격 48.

### Grid & Container
- 관리자 웹: 사이드 내비 240px + 본문. 본문 최대폭 1440px, 좌우 패딩 24.
- 기기 그리드: `repeat(auto-fill, minmax(280px, 1fr))`, gap 16.
- 모바일 앱: 좌우 패딩 20, 단일 컬럼.

### Density
관제 화면은 정보 밀도가 높아야 한다. 여백으로 고급스러움을 만들려 하지 말고,
**구분선과 정렬**로 만든다. 한 화면에서 스크롤 없이 기기 12대 상태가 보이는 것이
아름다운 여백보다 중요하다.

## Elevation & Depth

그림자는 **떠 있는 것에만** 쓴다 — 모달, 드롭다운, 토스트.
카드에는 그림자를 쓰지 않는다. 카드는 1px 테두리(`hairline`)로 구분한다.

```
overlay: 0 8px 24px rgba(16, 27, 38, 0.16)
dropdown: 0 4px 12px rgba(16, 27, 38, 0.12)
card: none
```

다크 모드에서는 그림자 대신 `surface-raised-dark` 밝기 차이로 레이어를 만든다.

## Shapes

라운드는 **4px 하나**가 기본이다(제안서 실치수 4pt와 동일). 예외는 두 가지뿐:
- 카드·모달·타일: 8px (`rounded.lg`)
- 배지·토글·아바타: pill / full

큰 카드에 20px 같은 과한 라운드를 쓰지 않는다. 산업용 제어 화면의 톤이 아니다.

## Components

### Device Card
기기 하나 = 카드 하나. 필수 구성 4요소:
1. 상태 점 + 상태 라벨 (좌상단)
2. 기기명 (`card-title`)
3. 대표 수치 1개 (`metric`) + 단위 (`metric-unit`)
4. 마지막 통신 시각 (`caption`, `body-muted`)

토글이 있으면 우상단 고정. 카드 전체가 클릭 영역이면 토글은 클릭 전파를 막는다.
알람 상태 카드는 테두리만 `state-error`로 바꾼다 — 배경을 빨갛게 칠하지 않는다.

### Status Badge
점(8px) + 라벨. 배경은 `state-*-bg`, **점은 `state-*` 본색, 글자는 `state-*-ink`.**
라벨 문구는 고정: `정상` / `점검` / `오류` / `오프라인` / `연결 중`.

### Toggle
52×32, thumb 28. ON은 `primary`, OFF는 `state-offline`.
**낙관적 UI를 쓰지 않는다.** IoT 명령은 실패할 수 있다. 토글을 누르면
`연결 중` 상태(thumb 위치 중간 + 스피너)를 거쳐 기기 응답 후 확정한다.
3초 내 응답 없으면 원위치 + 오류 토스트.

### Metric Tile
라벨(`label`, muted) 위, 수치(`metric-hero` 또는 `metric`) 아래, 단위는 수치 뒤 baseline 정렬.
증감 표시는 화살표 + 값, 색은 `state-online`/`state-error`가 아니라 **의미에 따라**
결정한다(전력 소비 증가는 나쁜 것이므로 상승이 초록이면 안 된다).

### Table
선 기반. 배경 줄무늬 없음. 헤더 아래 1px `hairline-strong`, 행 사이 1px `hairline`.
행 높이 52. 숫자 컬럼은 우측 정렬 + tabular-nums.

### Side Nav
`navy-sunken` 배경. 활성 항목은 `navy-raised` 면 + 좌측 2px `primary` 레일.
항목 높이 44 — 태블릿 터치 대응.

### Empty & Error State
기기가 없을 때 빈 화면을 그대로 두지 않는다.
아이콘 + 한 줄 설명 + 다음 행동 버튼(`기기 추가하기`) 세트로 제공한다.

## Do's and Don'ts

### Do
- 상태색은 기기 상태에만 쓴다
- 브랜드 블루는 누를 수 있는 것에만 쓴다
- 모든 상태를 색 + 텍스트 이중으로 표시한다
- 실시간 수치는 tabular-nums로 고정한다
- 터치 타겟은 최소 44×44
- 다크 모드에서 먼저 검증한다
- 명령 실행은 요청 → 진행 → 확정 3단계로 표현한다

### Don't
- 그라디언트를 장식으로 쓰지 않는다 (차트 채움은 예외)
- 카드에 그림자를 쓰지 않는다
- 면 + 테두리를 동시에 쓰지 않는다
- 색 하나로 상태를 전달하지 않는다
- 한 화면에 강조를 두 종류 이상 두지 않는다
- 본문 15px 미만으로 내리지 않는다
- 낙관적 토글(누르면 즉시 ON)을 쓰지 않는다

## Responsive Behavior

### Breakpoints
| 이름 | 폭 | 대상 |
|---|---|---|
| `sm` | < 640 | 모바일 앱 |
| `md` | 640–1023 | 태블릿 (현장 제어) |
| `lg` | 1024–1439 | 노트북 관리자 |
| `xl` | ≥ 1440 | 관제 데스크 / 벽면 디스플레이 |

### Collapsing Strategy
- `lg` 미만: 사이드 내비 → 햄버거 드로어
- `md`: 기기 그리드 2열, 표는 카드 리스트로 전환(가로 스크롤 금지)
- `sm`: 1열. 대표 수치 1개만 남기고 보조 지표는 상세 화면으로

### Wall Display (`xl` 이상)
3m 거리에서 읽힌다. `metric-hero` 44px → 72px로 승격,
상태 점 8px → 12px. 인터랙션 요소는 숨긴다(조작하는 화면이 아니다).

### Touch Targets
최소 44×44. 표 행 내 액션 아이콘은 시각적으로 20px이어도
히트 영역은 44px을 확보한다.

## Motion

- 상태 전환: 160ms `ease-out`
- 패널·드로어: 240ms `cubic-bezier(0.2, 0, 0, 1)`
- 연결 중 스피너: 1s 선형 반복
- 알람 발생 시 카드 테두리 1회 펄스(600ms). **반복 깜빡임은 금지** — 관제 피로.
- `prefers-reduced-motion` 존중: 모든 전환을 0ms로 축소하되 상태 변화는 즉시 반영.

## Accessibility

- 본문 대비 4.5:1, 큰 글자(18.66px/700 또는 24px/400 이상) 3:1 이상.
- 검증된 값 (WCAG 2.1 AA):

| 조합 | 대비 |
|---|---|
| 흰 글자 / `navy` | 14.30 |
| 흰 글자 / `primary-strong` | 5.21 |
| 흰 글자 / `state-error` | 4.95 |
| `body`(#333) / `canvas` | 12.63 |
| `body-muted`(#6B7280) / `canvas` | 4.83 |
| `body-muted-on-dark`(#9AA8BC) / `surface-dark` | 5.93 |
| `primary-subtle`(#66B2E0) / `navy` | 6.14 |
| `state-*-ink` / `state-*-bg` | 4.78 ~ 5.91 |
| `state-*-on-dark` / `surface-dark` | 5.02 ~ 6.81 |

- 흰 글자를 `primary`(#3A88B4) 위에 직접 올리지 않는다 → 3.92:1, AA 미달.
  `primary-strong`을 쓴다. 18px 이상 굵은 글자일 때만 `primary` 허용.
- `body-muted-on-dark`보다 어둡게 내리지 않는다.
- 상태는 색 + 텍스트 + 아이콘 형태 3중으로 구분한다.
- 포커스 링: 2px `focus-ring`(#66B2E0) + 2px offset. 절대 제거하지 않는다.
- 기기 제어 버튼에는 현재 상태를 `aria-pressed`로 노출한다.
- 알람은 `role="alert"`로 스크린리더에 즉시 전달한다.

## Iteration Guide

이 파일을 에이전트에게 줄 때:
1. 프로젝트 루트에 `DESIGN.md`로 복사한다.
2. "이 DESIGN.md를 따라 기기 목록 화면을 만들어줘"처럼 **화면 단위**로 지시한다.
3. 결과가 어긋나면 프롬프트를 고치지 말고 **이 파일의 해당 섹션을 고친다.**
   그래야 규칙이 누적된다.
4. 새 컴포넌트가 생기면 frontmatter `components:`에 토큰 참조 형태로 추가한다.

## Known Gaps

아직 이 문서가 정의하지 않은 것 — 필요해지면 채운다.
- 차트·그래프 상세 규격 (시계열 색 계열, 축 스타일)
- 지도/평면도 위 기기 배치 뷰
- 아이콘 세트 (현재 Lucide 기준 24px stroke 1.5 가정)
- 다국어(영문·일문) 시 한글 대비 줄바꿈 규칙
- 알림 센터·이력 타임라인
