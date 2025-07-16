# 250714

## Position(중요) !!!

### 1.  position 속성이란?
HTML 요소의 위치 지정 방식을 설정하는 속성입니다.
기본 흐름에서 벗어나 원하는 위치에 배치하거나,
상대적/절대적/고정 위치를 지정할 때 사용합니다.

### 2. 주요 속성값 비교
| 값       | 의미                           | 기준 요소            | 특징                                 |
|----------|--------------------------------|----------------------|--------------------------------------|
| `static` | 기본값 (기본 흐름)              | 없음                 | 위치 지정 불가 (`top`, `left` 무시됨) |
| `relative` | 자기 자신 기준으로 이동         | 자기 자신            | 문서 흐름 유지, 위치만 이동          |
| `absolute` | 가장 가까운 `position` 지정 요소 기준 | 부모 요소            | 문서 흐름에서 제거됨                 |
| `fixed` | 브라우저 창 기준 고정           | `viewport`           | 스크롤에도 위치 고정                 |
| `sticky` | 스크롤에 따라 `relative → fixed` 전환 | 부모 요소            | 조건 만족 시 고정됨 (`top` 등 지정 필요) |

### 3. 정리 해보기

| 값          | 쉽게 말하면…            | 기준이 되는 위치                 |
| ---------- | ------------------ | ------------------------- |
| `static`   | "기본 위치 그대로!"       | 없음 (기본 흐름)                |
| `relative` | "내 자리에서 조금만 옆으로\~" | 자기 자신                     |
| `absolute` | "부모 기준으로 자유롭게!"    | 가장 가까운 `position`이 지정된 부모 |
| `fixed`    | "스크롤해도 고정돼!"       | 브라우저 창(viewport)          |
| `sticky`   | "원래 있던 곳 → 고정!"    | 스크롤 조건 만족 시 부모 기준         |

- 음수값도 적용
- absoulte : 부모가 없다면 뷰포트가 기준
- 주의사항 z-index는 최소 relative 해주기 (position이 설정이 안되어있는 요소의 스타일엔 z-index 는 설정할 수 없다.)




### * 잘 몰랐던 것 

box-sizing: border-box;의미
| 속성                  | 크기 계산 방식                                  | 설명                          |
| ------------------- | ----------------------------------------- | --------------------------- |
| `content-box` (기본값) | `width`와 `height`는 **콘텐츠만**               | padding과 border는 크기 밖으로 더해짐 |
| `border-box`        | `width`와 `height`에 **padding과 border 포함** | box의 실제 크기를 유지하기 쉬움         |



---


# 250715
# Layout(중요) !!!


### 1. Flexbox란?
1차원 레이아웃 구성 (가로 or 세로 한 방향)
주로 정렬과 공간 분배에 강점
부모 요소에 display: flex 지정하여 사용


### 주요 속성 (부모 - Flex Container 기준)
| 속성                | 설명          | 예시                                      |
| ----------------- | ----------- | --------------------------------------- |
| `display: flex`   | Flexbox 활성화 | `display: flex;`                        |
| `flex-direction`  | 주축 방향 설정    | `row` (가로), `column` (세로)               |
| `justify-content` | 주축 방향 정렬    | `flex-start`, `center`, `space-between` |
| `align-items`     | 교차축 방향 정렬   | `stretch`, `center`, `flex-end`         |
| `flex-wrap`       | 줄바꿈 여부      | `nowrap` (기본), `wrap`                   |


### 주요 속성 (자식 - Flex Item 기준)
| 속성           | 설명                     | 예시 (간단 설명)                       |
| ------------ | ---------------------- | -------------------------------- |
| `flex`       | grow, shrink, basis 설정 | `flex: 1`, `flex: 0 1 auto` 등    |
| `order`      | 순서 변경                  | `order: 2` → 요소 순서 바뀜            |
| `align-self` | 개별 아이템 정렬              | `auto`, `flex-start`, `center` 등 |


# 250716
### 2. Grid란?
2차원 레이아웃 구성 (행 + 열)
정형적인 레이아웃, 대시보드 등에 적합
부모 요소에 display: grid 지정하여 사용

### 🧩 주요 속성 (부모 - Grid Container 기준)

CSS Grid를 사용할 때 자주 사용하는 속성들을 간단하게 정리한 표입니다.

| 속성                    | 설명                  | 예시                            |
|-------------------------|-----------------------|----------------------------------|
| `display: grid`         | Grid 시스템 활성화     | `display: grid;`                 |
| `grid-template-columns` | 열(컬럼) 정의          | `repeat(3, 1fr)`                 |
| `grid-template-rows`    | 행(로우) 정의          | `100px 200px`                    |
| `gap`                   | 행/열 간격             | `gap: 10px;`                     |
| `justify-items`         | 셀 내부 가로 정렬      | `start`, `center`, `end`        |
| `align-items`           | 셀 내부 세로 정렬      | `start`, `center`, `end`        |

---

### ✅ 예시 설명

- `repeat(3, 1fr)` : 동일한 너비의 열 3개를 생성
- `100px 200px` : 첫 번째 행은 100px, 두 번째 행은 200px
- `gap: 10px;` : 각 셀 사이에 10px 간격 부여
- `justify-items`, `align-items` : 각각 셀의 가로/세로 정렬 방식

---

### 📚 참고 자료
- [MDN Web Docs - CSS Grid](https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Grid_Layout)
- [CSS Tricks - A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)





===========
깃
온리 머지

일반 병합하기
패스트 포드 가능해도 새커밋 버튼 뉴르기

> 이렇게 되면 바뀐 시점으로 다시 병합해야 함
펑션1에서 다시 뎁2 병합 (이땨는 새커밋 필용없음)

리베이스 머지


깃플로우

