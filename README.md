# kdt-calendar

K-DeepTech Town — 공간 예약 시스템 (한국엔젤협회)

## 프로젝트 구조

```
kdt-calendar/
├── index.html       # 데스크톱 UI
├── m/
│   └── index.html   # 모바일 UI (/m)
└── vercel.json      # Vercel 배포 설정
```

## 기능 개요

- 크레딧 기반 공간 예약 (30분 슬롯 단위)
- 공간 4종: 3F.Room1 / 7F.Room1 / B1.Room1 / B1.Room2
- 관리자 승인 필요 공간 구분 처리
- 주간/일간/월간 캘린더 뷰 (데스크톱)
- 예약 확정 모달 및 크레딧 차감 미리보기
- 최근 예약 내역 표시

## 페이지

| 경로 | 설명 |
|---|---|
| `/` | 데스크톱 3단 레이아웃 UI |
| `/m` | 모바일 전용 UI |

## 변경 이력

### 2026-04-06
- 헤더 우측 상단 크레딧 배지 제거 (우측 패널과 중복)
- 전체 폰트를 Noto Sans KR로 통일 (DM Serif Display 제거)
- 모바일 UI 신규 추가 (`/m`)
  - 하단 탭 내비게이션 (홈 / 예약 / 내역)
  - 홈: 주간 날짜 스트립 + 선택일 일정 + 크레딧 요약
  - 예약: 공간 칩 선택 → 상세 카드 → 시간 입력 → 바텀 시트 확인
  - 내역: 상태별 필터 + 예약 카드 목록
  - Safe-area inset 대응 (노치/홈 인디케이터)

## 기술 스택

- 순수 HTML / CSS / JavaScript (프레임워크 없음)
- Google Fonts — Noto Sans KR
- Vercel 정적 호스팅
