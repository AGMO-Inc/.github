이 리포지토리는 조직(Organization) 전체에서 공통으로 사용할 **Issue/PR 템플릿 및 기본 설정(Community Health Files)** 을 관리합니다.

# 1. 공용 템플릿 만드는 방법

참고 : https://docs.github.com/ko/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates

## 1.1 md 파일로 만들기
- .md 파일로 만들면 해당 파일이 그대로 issue 템플릿으로 노출됩니다.
  
**예시**
- .github/ISSUE_TEMPLATE/example.md 파일 생성
```
---
name: 템플릿 이름
about: 템플릿 설명 (description)
title: "템플릿의 기본 제목"
labels: ''
assignees: ''
type: Document
---

# 예시 1

# 예시 2
- [ ] 개발할 기능 1
- [ ] 개발할 기능 2

```

- Issue 에서 템플릿이 노출되는지 확인

<img width="1310" height="937" alt="image" src="https://github.com/user-attachments/assets/e45947fb-7291-49c0-90cf-f02563de2ff8" />

## 1.2 yml 파일로 만들기
- .yml 파일로 만들면 해당 파일이 github 에 의해 해석되어 그대로 issue 포맷이 생성됩니다.
  
**예시**
- .github/ISSUE_TEMPLATE/example.yml 파일 생성
```
name: Bug Report
description: File a bug report.
title: "[Bug]: "
labels: ["bug", "triage"]
projects: ["octo-org/1", "octo-org/44"]
assignees:
  - octocat
type: bug
body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to fill out this bug report!
  - type: input
    id: contact
    attributes:
      label: Contact Details
      description: How can we get in touch with you if we need more info?
      placeholder: ex. email@example.com
    validations:
      required: false
  - type: textarea
    id: what-happened
    attributes:
      label: What happened?
      description: Also tell us, what did you expect to happen?
      placeholder: Tell us what you see!
      value: "A bug happened!"
    validations:
      required: true
  - type: dropdown
    id: version
    attributes:
      label: Version
      description: What version of our software are you running?
      options:
        - 1.0.2 (Default)
        - 1.0.3 (Edge)
      default: 0
    validations:
      required: true
  - type: dropdown
    id: browsers
    attributes:
      label: What browsers are you seeing the problem on?
      multiple: true
      options:
        - Firefox
        - Chrome
        - Safari
        - Microsoft Edge
  - type: textarea
    id: logs
    attributes:
      label: Relevant log output
      description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backticks.
      render: shell
  - type: checkboxes
    id: terms
    attributes:
      label: Code of Conduct
      description: By submitting this issue, you agree to follow our [Code of Conduct](https://example.com).
      options:
        - label: I agree to follow this project's Code of Conduct
          required: true

```

- Issue 에서 템플릿이 노출되는지 확인

<img width="1440" height="1209" alt="image" src="https://github.com/user-attachments/assets/2f787aad-23af-4cd7-bffa-50c3f151aa42" />
