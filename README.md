이 리포지토리는 조직(Organization) 전체에서 공통으로 사용할 **Issue/PR 템플릿 및 기본 설정(Community Health Files)** 을 관리합니다.

# 1. 공용 템플릿 만드는 방법

1) 이 리포지토리 이름은 반드시 `.github` 이어야 합니다.  
2) 기본 브랜치(default branch)에 아래 경로로 템플릿 파일을 추가합니다.

```
.github/ISSUE_TEMPLATE/
*.md 또는 *.yml

```

3) 커밋 후, 조직 내 각 레포지토리에서 **New issue**를 눌러 템플릿이 노출되는지 확인합니다.

### 동작 규칙(중요)
- 조직 공용 템플릿은 **각 레포에 별도 템플릿이 없을 때만** 적용됩니다.  
  (레포에 `.github/ISSUE_TEMPLATE/` 가 존재하면 해당 레포 템플릿이 우선 적용됩니다.)
- 템플릿에서 `labels:` 를 사용한다면, 각 레포에도 동일한 라벨이 존재해야 자동 부여됩니다.

## Directory

- `.github/ISSUE_TEMPLATE/` : 이슈 템플릿
- `.github/PULL_REQUEST_TEMPLATE.md` : PR 템플릿(선택)
- `.github/ISSUE_TEMPLATE/config.yml` : 이슈 작성 UI 설정(선택)
