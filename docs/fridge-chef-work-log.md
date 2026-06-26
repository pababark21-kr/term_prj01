# 프로젝트: 코디세이-냉장고파먹기 (자취생 냉장고 레시피 추천 앱)

## 1. 기획
- 서비스: 냉장고 재료 기반 AI 레시피 추천
- 타겟: 1인 가구 자취생
- 핵심 가치: 가진 재료로 바로 요리, 부족 재료는 장보기 안내

## 2. 디자인
- 톤앤매너: 미니멀 / 화이트 + 소프트 그린
- 화면 구성: 홈 → 레시피 목록 → 레시피 상세 (3단계)

## 3. 제작 과정
- 이미지 생성: GPT Image 2 (텍스트 깨짐 0건)
- 일관성 전략: 동일 톤/폰트/컬러 프롬프트 반복 적용
- 프로토타입: Figma (투명 핫스팟으로 화면 연결)

## 4. 산출물
- 프로토타입 링크: [코디세이-냉장고파먹기 프로토타입 보기](http://figma.com/proto/LJFKOHqUG00vgMj6fH9IuI/코디세이-냉장고파먹기-UI-UX?node-id=0-1&p=f&t=rsnmc3vy4TyHLBKn-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1)
- 화면 이미지 3종: 홈 / 목록 / 상세

## 5. 회고 (느낀 점)
- 잘된 점: 텍스트 깨짐 없이 한 번에 UI 이미지 생성
- 어려웠던 점: 기획 초기 아이디어 도출 단계. 명확한 근거 없이 '감'에 의존해 방향을 잡다 보니 의사결정에 확신이 부족했다.
- 개선 아이디어: 시장조사·사용자 인터뷰를 선행해 기획을 객관적 지표 기반으로 수립하면, 이후 디자인·기능 판단도 감이 아닌 데이터로 내릴 수 있을 것이다.

## 6. 사용한 프롬프트 및 모델

[홈 화면 - 초안 v1]
프롬프트: 
A clean minimal mobile app UI design for a recipe recommendation app,
home screen, white background with soft green accent colors,
top greeting text and search bar,
ingredient input area with rounded tag chips (like "egg", "onion", "rice"),
a large "Find Recipes" button at the bottom,
modern flat design, plenty of white space,
9:16 aspect ratio, high quality UI mockup

의도: 미니멀 톤 / 재료 입력 중심 / 9:16
→ 결과 확인 후 수정 예정

[목록 화면 - 초안 v1]
프롬프트: 
A clean minimal mobile app UI design for a recipe recommendation app,
recipe list screen, keep the same design style as the reference image,
white background with soft green accent colors,
top header with back arrow and title "Recipes for you",
a short subtitle "Based on your ingredients",
2 to 3 vertical recipe cards, each card contains:
a food photo on the left, recipe name in bold,
cooking time and difficulty level with small icons,
and a green "ingredient match" percentage badge,
rounded cards, generous white space, modern flat design,
bottom navigation bar with 4 icons (Home, Explore, Favorites, Profile),
9:16 aspect ratio, high quality UI mockup
일관성 전략: 홈 화면 첨부 + "same design style as reference"
의도: 카드형 목록 / 재료 일치율 강조

[상세 화면 - 초안 v1]
프롬프트:
A clean minimal mobile app UI design for a recipe recommendation app,
recipe detail screen, keep the same design style as the reference image,
white background with soft green accent colors,
large food photo at the top (finished dish),
recipe title in bold below the image with cooking time and difficulty,
a section "Ingredients" showing ingredient chips,
some chips marked as missing in light orange,
a "Steps" section with numbered cooking instructions,
rounded cards, generous white space, modern flat design,
a green "Start Cooking" button at the bottom,
9:16 aspect ratio, high quality UI mockup
일관성 전략: 동일 (레퍼런스 첨부)
의도: 완성 요리 사진 강조 / 부족 재료 주황 표시

[영어로 생성된 UI 이미지를 한국어로 패치]
프롬프트:
@이미지 만들기 '한국어' 버전으로 다시 생성해줘. * 번역이 어색하지 않게 현지어 느낌을 잘 살려야해. 그리고 한글깨짐 없이 깔끔하게 생성되어야 해.
일관성 전략: 이미 생성된 UI 이미지 첨부
의도: 한국어 버전을 어색하지 않게 번역해서 깨짐없이 생성하기

[사용 모델]
* 기획: Claude Opus 4.8
* 이미지 생성: GPT Image 2

---

# 개선 적용: HEX 색상 명시 / 폰트 통일 / 안전영역 / 기획 핵심가치(장보기) 연결

## 1️⃣ 홈 화면 [v2]

```
A clean minimal mobile app UI design for a recipe recommendation app, home screen.
White background (#FFFFFF) with soft green accent (#A8D5BA), text in dark gray (#333333).
Consistent sans-serif typography throughout.
Include iOS status bar at top, all content within safe area.

Top: a friendly greeting text "What's in your fridge?".
Main: an ingredient input area with rounded tag chips ("egg", "onion", "rice"),
each chip has a small remove "x", and a clear "+" add button to add new ingredients.
Placeholder text "Add your ingredients to start" when area looks light.
A small counter "3 ingredients added".
Bottom: a large primary green "Find Recipes" button.
NO separate search bar (ingredient input is the only entry method).

Modern flat design, plenty of white space, 9:16 aspect ratio, high quality UI mockup. (Korean version)
```
**핵심 변경**: 검색바 제거(역할 중복 해소) / "+" 추가버튼 명시 / 재료 카운터 추가


## 2️⃣ 목록 화면 [v2]

```
A clean minimal mobile app UI design for a recipe recommendation app, recipe list screen.
Keep the same design style as the reference image.
White background (#FFFFFF) with soft green accent (#A8D5BA), text in dark gray (#333333).
Consistent sans-serif typography. Include status bar and safe area.

Top header: back arrow, title "Recipes for you", subtitle "Based on your ingredients".
A horizontal filter chip row: "Quick", "Vegetarian", "Under 15 min".
Exactly 3 vertical recipe cards. Each card contains:
a food photo on the left, recipe name in bold,
cooking time and difficulty with small icons,
a green "match" badge showing percentage (e.g. "92% match"),
and a small supporting text below "4 of 5 ingredients you have".
Rounded cards, generous white space, modern flat design.
Bottom navigation bar with 4 icons (Home, Explore, Favorites, Profile).

9:16 aspect ratio, high quality UI mockup. (Korean version)
```
**핵심 변경**: 카드 정확히 3개 고정 / 필터칩 추가 / match% 근거 텍스트("4 of 5") 추가


## 3️⃣ 상세 화면 [v2]

```
A clean minimal mobile app UI design for a recipe recommendation app, recipe detail screen.
Keep the same design style as the reference image.
White background (#FFFFFF) with soft green accent (#A8D5BA), text in dark gray (#333333).
Consistent sans-serif typography. Include status bar and safe area.

Top: large food photo of the finished dish.
Below: recipe title in bold, with cooking time, difficulty, and serving size "1 person" and calories info.
"Ingredients" section showing ingredient chips,
some chips marked as missing in light orange (#F5C396),
and an "Add to shopping list" link button next to the missing ingredients.
"Steps" section with exactly 3 numbered cooking instructions.
Rounded cards, generous white space, modern flat design.
Bottom: a green "Start Cooking" button.

9:16 aspect ratio, high quality UI mockup. (Korean version)
```
**핵심 변경**: 1인분/칼로리 추가 / **"장보기 담기" 버튼**(기획 핵심가치 연결!) / 스텝 3개 고정


## 📋 v1 → v2 변경 요약표

| 항목 | v1 | v2 |
|---|---|---|
| 색상 | "soft green" (추상적) | `#A8D5BA` 등 HEX 명시 |
| 안전영역 | 없음 | status bar + safe area |
| 홈 입력 | 검색바+칩 중복 | 칩만 + "+"버튼 |
| 목록 카드 | "2~3개" 모호 | **정확히 3개** + 필터칩 |
| match% | 숫자만 | **근거 텍스트** 추가 |
| 상세 장보기 | 주황 표시만 | **장보기 버튼 연결** 🎯 |
