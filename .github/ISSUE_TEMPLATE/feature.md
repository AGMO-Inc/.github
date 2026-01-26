name: "기능"
description: "새 기능/개선 작업 제안 및 구현 계획"
title: "[Feature] "
labels: ["type/feature"]
body:
  - type: textarea
    id: summary
    attributes:
      label: "한 줄 요약"
      description: "무엇을 왜 하는지 한 문장"
      placeholder: "예) 북마크 기본 폴더명을 '기본'으로 고정한다"
    validations:
      required: true

  - type: textarea
    id: background
    attributes:
      label: "배경 / 문제"
      description: "현재 상황과 문제점을 적어주세요"
      placeholder: "- 현재:\n- 문제:\n- 목표(성공 기준):"
    validations:
      required: true

  - type: textarea
    id: scope
    attributes:
      label: "범위 (In / Out)"
      placeholder: "In:\n- \n\nOut:\n- "
    validations:
      required: true

  - type: textarea
    id: requirements
    attributes:
      label: "요구사항"
      description: "기능이 만족해야 하는 조건/규칙"
      placeholder: "- [ ] \n- [ ] "
    validations:
      required: true

  - type: textarea
    id: design
    attributes:
      label: "설계/접근"
      description: "대략적인 설계, API, 데이터 구조, 흐름 등"
      placeholder: "- 화면/플로우:\n- API 변경:\n- DB/이벤트:\n- 권한/에러 처리:"
    validations:
      required: false

  - type: textarea
    id: todo
    attributes:
      label: "작업 항목 (To-do)"
      placeholder: "- [ ] 분석\n- [ ] 구현\n- [ ] 테스트\n- [ ] 문서/배포"
    validations:
      required: true

  - type: textarea
    id: risks
    attributes:
      label: "리스크 / 의존성"
      placeholder: "- 리스크:\n- 의존성(다른 이슈/PR):"
    validations:
      required: false

  - type: textarea
    id: references
    attributes:
      label: "참고 링크"
      placeholder: "- 관련 이슈/문서/스펙 링크"
    validations:
      required: false
