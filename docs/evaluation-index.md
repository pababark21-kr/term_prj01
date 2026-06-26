# 평가 기준 대응표 - 냉장고 파먹기 / fridge-chef

## 최종 제출 대상

- 프로젝트명: 냉장고 파먹기 / fridge-chef
- 유형: AI 기반 모바일 UI/UX 디자인 시안
- 화면 구성: 메인 화면 -> 레시피 목록 화면 -> 레시피 상세 화면
- 최종 UI 이미지:
  - [메인 화면](../assets/final-ui/01-main-screen.jpg)
  - [목록 화면](../assets/final-ui/02-list-screen.jpg)
  - [상세 화면](../assets/final-ui/03-detail-screen.jpg)
- 작업 로그: [fridge-chef-work-log.md](fridge-chef-work-log.md)
- Figma 프로토타입: [코디세이-냉장고파먹기 프로토타입 보기](http://figma.com/proto/LJFKOHqUG00vgMj6fH9IuI/코디세이-냉장고파먹기-UI-UX?node-id=0-1&p=f&t=rsnmc3vy4TyHLBKn-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1)

## 평가 항목별 대응표

| 평가 항목 | 충족 여부 | 증빙 위치 | 설명 |
| --- | --- | --- | --- |
| 1. UI 디자인 이미지 3장 이상 및 화면 역할 구분 | 충족 | [메인 화면](../assets/final-ui/01-main-screen.jpg), [목록 화면](../assets/final-ui/02-list-screen.jpg), [상세 화면](../assets/final-ui/03-detail-screen.jpg), [fridge-chef-work-log.md](fridge-chef-work-log.md) | 메인, 목록, 상세 3개 화면이 각각 최종 이미지로 저장되어 있고 작업 로그에서 홈 -> 레시피 목록 -> 레시피 상세 3단계 구성을 설명합니다. |
| 2. 이미지 내 텍스트 깨짐/가독성 수정 여부 | 충족 | [fridge-chef-work-log.md](fridge-chef-work-log.md), [qa-checklist.md](qa-checklist.md) | 작업 로그에 텍스트 깨짐 0건과 한국어 버전 재생성 프롬프트가 기록되어 있고, QA 체크리스트에서 텍스트 깨짐 수정을 확인합니다. |
| 3. Figma 화면 배치 및 Hotspot/전환 흐름 | 충족 | [fridge-chef-work-log.md](fridge-chef-work-log.md), [final-submission-links.md](final-submission-links.md), Figma 프로토타입 링크 | repo 내부 문서에 냉장고 파먹기 Figma 프로토타입과 투명 핫스팟 화면 연결 기록이 있습니다. 외부 Figma 내용을 직접 열람했다고 가정하지 않습니다. |
| 4. 사용자 목표와 핵심 플로우 3단계 설계 이유 | 충족 | [work-log.md](work-log.md), [design-decision-log.md](design-decision-log.md), [fridge-chef-work-log.md](fridge-chef-work-log.md) | 재료 입력 -> 추천 레시피 비교 -> 상세 조리/부족 재료 확인 흐름으로 사용자 목표를 설명합니다. |
| 5. 화면 3종의 정보 구조와 우선순위/동선 배치 기준 | 충족 | [work-log.md](work-log.md), [design-decision-log.md](design-decision-log.md) | 메인, 목록, 상세 화면별 주요 정보와 CTA, 카드, 부족 재료 안내 배치 기준을 정리했습니다. |
| 6. 프롬프트 단계적 수정 과정과 문제 해결 과정 | 충족 | [prompt-log.md](prompt-log.md), [fridge-chef-work-log.md](fridge-chef-work-log.md) | 초안과 수정1 단계의 프롬프트, 문제점, 수정 방향, 변경 이유가 화면별로 기록되어 있습니다. |
| 7. 후가공 수행 방식과 선택 이유 | 충족 | [work-log.md](work-log.md), [design-decision-log.md](design-decision-log.md), [fridge-chef-work-log.md](fridge-chef-work-log.md) | Figma에서 화면 배치, 전환 흐름, Hotspot, 텍스트 가독성 및 정렬 검수를 수행한 이유를 설명합니다. |
| 8. 프롬프트 구성 요소가 결과물에 미친 영향 | 충족 | [prompt-log.md](prompt-log.md), [work-log.md](work-log.md) | 색상, 9:16 화면비, safe area, 카드 수, 일치율 근거, 장보기 연결 등 프롬프트 구성 요소와 결과 변화가 대응됩니다. |
| 9. AI 생성 이미지의 한계 진단 및 재발 방지 전략 | 충족 | [work-log.md](work-log.md), [design-decision-log.md](design-decision-log.md), [qa-checklist.md](qa-checklist.md) | 텍스트 깨짐, 모호한 색상, 역할 중복, 일관성 흔들림을 한계로 진단하고 HEX 색상, 폰트, safe area, 화면별 검수 전략으로 대응합니다. |
| 10. 일관성 유지 전략 선택 이유 및 적용 방법 | 충족 | [fridge-chef-work-log.md](fridge-chef-work-log.md), [design-decision-log.md](design-decision-log.md), [prompt-log.md](prompt-log.md) | 동일 톤/폰트/컬러 프롬프트, 9:16 화면비, 카드/버튼/여백 규칙을 반복 적용한 이유와 방식을 기록했습니다. |
| 11. 적용 전후 비교 근거를 통한 일관성 개선 설명 | 충족 | [prompt-log.md](prompt-log.md), [work-log.md](work-log.md), [fridge-chef-work-log.md](fridge-chef-work-log.md) | v1 -> v2 변경 요약과 최종 채택 기준을 통해 검색바 제거, 카드 3개 고정, 장보기 연결 등 전후 개선 근거를 설명합니다. |

## 참고 사항

- EcoTrack은 참고/보조 시안이며, 이 대응표의 최종 평가 대상은 냉장고 파먹기 / fridge-chef입니다.
- 외부 Google Drive/Figma 링크의 실제 내용을 직접 열람했다고 판단하지 않고, repo 내부 문서에 기록된 링크와 파일 경로를 기준으로 정리했습니다.
