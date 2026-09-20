# 클로드 디자인 스킬 연결 가이드

릴스(`cutoven.ai`)에서 본 세 번째 스킬은 **`ui/ux promax`** 입니다.
검색해서 실물을 확인했고, 이 문서에 설치법과 검증 결과를 정리했습니다.

---

## 1. UI/UX Pro Max — 릴스에서 본 그 스킬

- 저장소: https://github.com/nextlevelbuilder/ui-ux-pro-max-skill
- 라이선스 MIT · 무료 · Python
- **직접 확인한 값** (2026-09-20 GitHub API 조회): ⭐ 129,092 · fork 13,758 · 전날에도 커밋

> 국내 소개 글 일부가 "38,100 스타"라고 쓰는데 오래된 수치입니다. 실제로는 12.9만입니다.

### 실물 확인 결과

클론해서 스크립트를 직접 돌려봤습니다. 마케팅 문구가 아니라 **실제 CSV 데이터 + Python 검색기**입니다.

| 데이터 | 행 수 |
|---|---|
| `google-fonts.csv` | 1,934 |
| `colors.csv` / `products.csv` / `ui-reasoning.csv` | 각 192 |
| `ux-guidelines.csv` | 119 |
| `icons.csv` | 105 |
| `styles.csv` | 88 |
| `typography.csv` | 74 |

모델이 기억에서 지어내는 게 아니라 로컬 CSV를 조회해 답한다는 점이 이 스킬의 핵심입니다.

### 설치 (셋 중 하나)

```bash
# A. 플러그인 마켓플레이스 — Claude Code 안에서
/plugin marketplace add nextlevelbuilder/ui-ux-pro-max-skill

# B. CLI
npx ui-ux-pro-max-cli init --ai claude

# C. 수동 — 필요한 스킬 하나만
git clone --depth 1 https://github.com/nextlevelbuilder/ui-ux-pro-max-skill.git
cp -r ui-ux-pro-max-skill/.claude/skills/ui-ux-pro-max ~/.claude/skills/
```

**C를 권합니다.** 저장소에는 스킬이 7종 들어 있고 전부 설치하면 10MB가 넘습니다.

| 스킬 | 크기 |
|---|---|
| `ui-styling` | 5.8M |
| **`ui-ux-pro-max`** | **3.8M** |
| `design` | 388K |
| `design-system` | 272K |
| `brand` | 164K |
| `slides` | 40K |
| `banner-design` | 24K |

필요한 것만 `~/.claude/skills/`에 넣으면 모든 프로젝트에서 잡힙니다.

> **복제본 주의.** 이름과 설명(스타일 84종·팔레트 192개·폰트 74쌍…)이 거의 같은
> 파생 저장소가 여럿 있습니다. 예: `nicohodt/claude-code-ui-ux-skill`(⭐5).
> 설치는 반드시 원본 `nextlevelbuilder/ui-ux-pro-max-skill`(⭐129,092)에서 합니다.

### 직접 조회해보기

```bash
python3 ~/.claude/skills/ui-ux-pro-max/scripts/search.py \
  "IoT device control dashboard dark" --domain style -n 2
```

`--domain`: `style` `color` `chart` `landing` `product` `ux` `typography` `icons` `gsap` `react` `web` `google-fonts`
`--stack`: React, Next.js, Vue, Svelte, SwiftUI, Flutter, Jetpack Compose 등 22종

---

## 2. awesome-design-md — 같이 언급되는 다른 것

### "연결"이 아니다

`awesome-design-md`는 MCP 커넥터도, 설치형 플러그인도 아니다.
**마크다운 파일 한 장을 프로젝트 루트에 복사하는 것**이 전부다.
계정 연동이나 인증 절차는 없다.

- 원본 저장소: https://github.com/VoltAgent/awesome-design-md (74종)
- 스킬 패키지 버전: https://github.com/wwewtech/awesome-design-skills

### 세 가지 사용 경로

**1) Claude Code (로컬, 권장)**

```bash
# 컬렉션 받기
git clone --depth 1 https://github.com/VoltAgent/awesome-design-md.git

# 원하는 것 하나를 내 프로젝트 루트에 복사
cp awesome-design-md/design-md/linear/DESIGN.md ~/my-project/DESIGN.md
```

이후 "이 DESIGN.md 따라서 기기 목록 화면 만들어줘"라고 지시하면 된다.
항상 자동 참조되게 하려면 `CLAUDE.md`에 한 줄 추가한다.

```markdown
UI 작업 시 프로젝트 루트의 `DESIGN.md` 토큰을 반드시 따른다.
```

**2) 스킬로 상시 설치**

```bash
git clone --depth 1 https://github.com/wwewtech/awesome-design-skills.git
cp -r awesome-design-skills/<skill-dir> ~/.claude/skills/
```

`~/.claude/skills/`에 두면 모든 프로젝트에서 자동으로 잡힌다.

**3) Claude Design (웹)**

파일 시스템이 없으므로 대화창에 `DESIGN.md`를 **첨부**하거나 본문에 붙여넣는다.
디자인 시스템 프로젝트를 만들어 두면 매번 붙여넣지 않아도 된다.

---

## 3. 이 폴더가 제안하는 것

74종 중 하나를 그대로 쓰면 결과물은 "스트라이프처럼 생긴 우리 제품"이 된다.
데모·목업 속도에는 유리하지만 브랜드 자산은 쌓이지 않는다.

그래서 **포맷만 빌리고 내용은 마인드 것**으로 채운 파일을 함께 넣었다.

| 파일 | 내용 |
|---|---|
| `MIND-DESIGN.md` | 마인드 IoT 연동 플랫폼용 디자인 시스템 명세 |
| `preview.html` | 토큰·컴포넌트 시각 확인용 (다크/라이트 토글) |

기반은 기존 제안서 PPT 규격(`ppt-design-system-v2`)과 동일한 토큰이다.
네이비 `#1B2B41`, 브랜드 블루 `#3A88B4`, Pretendard, 라운드 4pt.
**제안서와 실제 제품 화면이 같은 얼굴을 갖는다**는 것이 이 방식의 핵심 이점이다.

### 쓰는 법

```bash
cp design/MIND-DESIGN.md <내-프로젝트>/DESIGN.md
```

### 화면 유형이 아니라 규칙을 고친다

결과가 마음에 안 들 때 프롬프트를 길게 쓰지 말고
`MIND-DESIGN.md`의 해당 섹션을 고친다. 그래야 규칙이 누적되고,
디자이너 2명이 같은 기준을 공유하게 된다.

## 4. 둘은 경쟁 관계가 아니다

| | 역할 | 아는 것 / 모르는 것 |
|---|---|---|
| **UI/UX Pro Max** | 보편적 설계 규칙 | 대비·터치타겟·로딩 상태·반응형은 알지만, **마인드 브랜드는 모른다** |
| **MIND-DESIGN.md** | 우리 정체성 | 네이비·브랜드블루·Pretendard·기기 상태 규칙은 알지만, 일반 UX 지식은 없다 |

같이 쓰면 된다. 스킬이 "이 버튼 대비가 부족하다"를 잡고,
`DESIGN.md`가 "그럼 `primary-strong #2F7399`를 쓴다"를 정한다.

스킬만 쓰면 잘 만들어졌지만 아무 회사나 쓸 수 있는 화면이 나온다.
`DESIGN.md`만 쓰면 브랜드는 맞지만 UX 기본기를 놓친다.

## 5. 접근성 검증 기록

`MIND-DESIGN.md`의 색 조합은 WCAG 2.1 AA 기준으로 계산 검증했다.
검증 과정에서 실제로 세 가지가 걸렸고, 그에 맞춰 토큰을 분리했다.

| 문제 | 조치 |
|---|---|
| 브랜드 블루 `#3A88B4` 위 흰 글자 = 3.92:1 (AA 미달) | 면은 `#3A88B4` 유지, 흰 글자가 올라가는 곳만 `primary-strong #2F7399`(5.21:1) |
| 상태 본색을 배지 글자로 쓰면 2.66~4.26:1 (미달) | `state-*-ink` 계열 신설 (4.78~5.91:1) |
| 다크 배경 위 상태색 판별 어려움 | `state-*-on-dark` 계열 신설 (5.02~6.81:1) |

재검증:

```bash
python3 - <<'PY'
def lum(h):
    h=h.lstrip('#'); c=[int(h[i:i+2],16)/255 for i in (0,2,4)]
    c=[x/12.92 if x<=0.03928 else ((x+0.055)/1.055)**2.4 for x in c]
    return 0.2126*c[0]+0.7152*c[1]+0.0722*c[2]
def cr(a,b):
    l1,l2=sorted([lum(a),lum(b)],reverse=True); return round((l1+0.05)/(l2+0.05),2)
print(cr('#FFFFFF','#2F7399'))   # 5.21  기본 버튼
print(cr('#15795A','#E7F5EF'))   # 4.78  정상 배지
PY
```
