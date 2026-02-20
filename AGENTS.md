---
type: custom
---
# AGENTS.md

This file is the working agreement for humans and automation (CI, bots, AI agents).

## Project Overview and Description

- 이 레포는 AGMO 조직의 공용 GitHub 설정 레포지토리다.
- 주요 대상은 이슈/PR 템플릿, 재사용 가능한 GitHub Actions 워크플로, 에이전트 설정(AGENTS.md/.agents)이다.
- 애플리케이션 런타임 코드보다 CI/CD 자동화와 협업 프로세스 일관성을 관리하는 목적이 크다.

## Tools, Technologies, and Frameworks Used

- GitHub Actions (reusable workflow, workflow_call)
- YAML 기반 템플릿/워크플로 관리
- GitHub CLI (`gh`) 기반 이슈/PR/런 조회 및 자동화
- OpenAI `codex-action` 연동 워크플로

## How to Build and Run Tests

- Build: 별도 애플리케이션 빌드 단계 없음(설정/워크플로 레포)
- Validation:
  - 전체 워크플로 점검: `actionlint .github/workflows/*.yml` (설치된 경우)
  - 변경점 확인: `git diff`
  - GitHub Actions 런 확인: `gh run list` / `gh run view <run-id>`
- Test: 별도 테스트 스위트 없음. 워크플로 실행 결과와 로그 검증으로 대체.

## 기본 원칙

- 모든 응답은 한국어로 작성한다.
- 작업 시작/진행/정리 과정에서 TODO-Issue.md 를 단일 진실원천(SSOT)으로 사용한다.
- TODO-Issue.md 에는 "현재 작업 중인 GitHub Issue"에 대한 실행 과제를 기록한다.
- 모든 Git 작업(브랜치 생성/커밋/푸시/PR/리베이스)은 기본적으로 `develop` 또는 `develop` 하위 브랜치에서 수행한다.
- `main`/`master`에서 Git 작업이 필요할 경우에는 사용자에게 명시적으로 허락을 받은 뒤에만 수행한다.

## 레포/프로젝트 정보

- 조직: AGMO-Inc
- 프로젝트명: 관련없음
- 프로젝트 url: N/A
- 레포: git@github.com:AGMO-Inc/.github.git

## 스킬

- 실행 절차(이슈 시작, 커밋, 푸시/PR 등)는 `.agents/` 하위 스킬을 참고한다.
- 문서 중복을 피하기 위해 본 파일에는 절차 상세를 중복 기재하지 않는다.
