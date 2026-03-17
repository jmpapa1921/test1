# CLAUDE.md — Project MERCENARY

## 프로젝트 개요
Area 88 오마주 PC용 횡스크롤 슈팅 게임.
엔진: Godot 4.x / 언어: GDScript

## 디렉토리 구조
```
src/scenes/    — Godot 씬 파일 (.tscn)
src/scripts/   — GDScript 파일 (.gd)
src/assets/    — 스프라이트, 사운드, 폰트
docs/design/   — 설계 문서
docs/art/      — 아트 가이드, 레퍼런스
tasks/         — 개발 태스크 목록
```

## 코딩 규칙
- 씬 이름: PascalCase (예: PlayerShip.tscn)
- 스크립트 이름: snake_case (예: player_ship.gd)
- 신호(Signal) 이름: snake_case, 동사로 시작 (예: health_changed)
- 상수: UPPER_SNAKE_CASE

## 핵심 시스템 우선순위
1. 플레이어 이동 및 사격
2. 경제 시스템 (자금 획득/지출)
3. 기체 관리 (구매/손실/교체)
4. 적 AI 및 웨이브 스폰
5. 보스 패턴

## Claude에게 요청 시 주의사항
- 새 씬/스크립트 작성 전 설계 먼저 확인
- Godot 4 기준으로 작성 (Godot 3 문법 사용 금지)
- 성능: 적 50기 동시 처리 가능하도록 오브젝트 풀링 적용
