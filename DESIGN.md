---
version: alpha
name: AYOCODING
description: 토스처럼 깨끗한 흰 바탕 + 아요코딩 로고 파랑. 큰 한글 제목, 넉넉한 여백, 부드러운 움직임.
colors:
  primary: "#3182F6"
  primary-dark: "#1B64DA"
  primary-light: "#E8F3FF"
  ink: "#191F28"
  body: "#4E5968"
  muted: "#6B7684"
  line: "#E5E8EB"
  surface: "#F9FAFB"
  white: "#FFFFFF"
  logo-navy: "#1E2A5A"
typography:
  h1:
    fontFamily: Pretendard Variable
    fontSize: 66px
    fontWeight: 800
    lineHeight: 1.25
    letterSpacing: "-0.04em"
  h2:
    fontFamily: Pretendard Variable
    fontSize: 52px
    fontWeight: 800
    lineHeight: 1.3
    letterSpacing: "-0.035em"
  body-lg:
    fontFamily: Pretendard Variable
    fontSize: 20px
    fontWeight: 400
    lineHeight: 1.7
  label:
    fontFamily: Pretendard Variable
    fontSize: 17px
    fontWeight: 700
rounded:
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  pill: 99px
spacing:
  section: 140px
  section-mobile: 96px
  gutter: 24px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.white}"
    rounded: "{rounded.md}"
    height: 56px
  button-primary-hover:
    backgroundColor: "{colors.primary-dark}"
    textColor: "{colors.white}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    height: 56px
  tag:
    backgroundColor: "{colors.primary-light}"
    textColor: "{colors.primary-dark}"
    rounded: "{rounded.pill}"
  card:
    backgroundColor: "{colors.white}"
    textColor: "{colors.body}"
    rounded: "{rounded.lg}"
    padding: 32px
  footer:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.body}"
  wordmark:
    textColor: "{colors.logo-navy}"
  hint:
    backgroundColor: "{colors.white}"
    textColor: "{colors.muted}"
  divider:
    backgroundColor: "{colors.line}"
---

## Overview

아요코딩 회사 홈페이지(ayocoding.co.kr) 디자인 기준. 참고: 토스 홈페이지(큰 제목·여백·스크롤 등장), Supahero(첫 화면이 가장 중요 — PC는 왼쪽 글 + 오른쪽 앱 화면 2단), GDWEB(한국형 굵은 한글 타이포 + 숫자 띠), Webzibition(마우스에 반응하는 인터랙션). 다음에 고칠 때 이 파일을 먼저 읽고 같은 규칙으로 만든다.

## Colors

- **Primary #3182F6** — 버튼·강조 단어·아이콘. 아요코딩 로고 파랑과 맞춤.
- **Ink #191F28 / Body #4E5968 / Muted #6B7684** — 제목·본문·보조 글. 작은 글씨에 #8B95A1 은 쓰지 않는다(대비 부족).
- **Logo navy #1E2A5A** — 메뉴줄 'AYO' 글자(로고 글자판과 같은 색).
- **#FF6B4A** — 측정 그림의 각도 표시(글자 아님)에만.
- 파랑 버튼 위 흰 글자는 대비 3.7:1(토스와 같음) — 버튼 글자는 굵게(600 이상) 유지.
- 메디컬링크 구역만 어두운 바탕(#191F28) + 밝은 파랑(#64A8FF).

## Typography

Pretendard(jsDelivr CDN). 제목은 굵게(800)·자간 좁게, 본문은 17~20px·줄간 1.7. 한글은 `word-break: keep-all`.

## Layout

- 최대 폭 1140px, 좌우 24px. 섹션 위아래 140px(모바일 96px).
- 첫 화면: PC(1000px 이상) 2단 — 왼쪽 문구·버튼·신뢰 문구, 오른쪽 앱 화면 3장 부채꼴. 모바일은 가운데 정렬 한 줄.
- 기능 소개: 글과 앱 화면이 좌우를 번갈아.
- 첫 화면 아래 숫자 띠(사실인 숫자만: 측정 4종, 관절 7곳, 사진 1장).

## Elevation & Depth

그림자는 앱 화면 카드에만: `0 30px 60px -20px rgba(25,31,40,.25)`. 나머지는 선(#E5E8EB)과 배경색 차이로 구분.

## Shapes

버튼 16px, 카드 24px, 앱 화면 28px, 큰 상자 32px, 태그는 완전 둥글게.

## Components

- 버튼: 파랑 채움(주) / 회색 채움(보조). 높이 56px. 주 버튼에 → 화살표, 마우스 올리면 오른쪽으로 이동.
- 아이콘: 이모지 대신 선 아이콘(SVG, 굵기 2, 둥근 끝, `.ico` 클래스, 글자색 따라감).
- 움직임: 스크롤 등장(.rv), 배경 빛 떠다님, 앱 화면 둥둥·스캔선, 기능 이름 흐르는 띠, 측정 3단계 SVG, 숫자 올라가기, PC 마우스 3D 기울기(.tilt). `prefers-reduced-motion`이면 전부 끔.

## Do's and Don'ts

- Do: 저장소에서 확인되는 기능·문구만 쓴다(바디샷 store/play 캡션, 메디컬링크 소개).
- Do: 앱 화면 그림은 posture-check/store/play 스크린샷을 잘라 쓴다.
- Don't: 측정값·사용자 수·효과를 지어내지 않는다. 그림 속 숫자는 실제 앱 화면에 있는 것만.
- Don't: '진단' 표현 금지 — '참고 자료'.
- Don't: 이모지 아이콘, 3가지 넘는 강조색.
