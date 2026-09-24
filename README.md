# Clovy

일상 속 작은 행복과 행운을 발견하고 기록하도록 돕는 **저부담 AI Journaling App**

- Role: Product Manager / Product Designer
- Period: 2026.01 - Present
- Platform: iOS
- Status: App Store 출시 

---

## 1. 문제

**155+건의 사용자 서베이와 리뷰 데이터, 선행논문 연구**를 통해 감사일기를 시작하고 이어가는 과정에서 다음과 같은 부담을 발견했습니다.

- 기록을 시작하기 전, 자신의 하루에서 **무엇을 기록할지 직접 찾아내고 판단해야 하는 부담**
- 비슷한 내용이 반복될 때 **지금처럼 기록해도 되는지에 대한 혼란**
- 연속 기록 중심의 방식에서는 기록을 쉬었을 때 **다시 시작하기 어려워지는 부담**

이를 바탕으로 핵심 문제를 다음과 같이 정의했습니다.

> **어떻게 하면 사용자가 기록을 잘 해야 한다는 부담 없이,  
> 자신의 일상 속 Happy / Lucky Moment를 발견하고 기록할 수 있을까?**

---

## 2. 해결방법

### ① Moment가 떠오르는지에 따라 작성 Flow 분리

기록할 Moment가 이미 있는 사용자에게 AI 사용을 강제하지 않고, 필요한 경우에만 도움을 받을 수 있도록 두 가지 Flow를 설계했습니다.

**Direct Input**  
Moment 직접 작성 → Happy / Lucky 선택 → 저장

**AI-assisted Discovery**  
하루에 있었던 일을 자유롭게 작성 → AI가 **작성 내용 안에서 Happy / Lucky Moment를 탐색** → 해당 부분 Highlight → Happy / Lucky 여부와 판단 이유 설명 → 사용자 확인 → Entry 작성

이를 통해 AI가 새로운 경험을 만들어내는 것이 아니라, **사용자가 이미 경험하고 작성한 내용 안에서 놓쳤던 Moment를 발견하도록 보조**했습니다.

### ② AI가 발견하되, 최종 기록은 사용자가 자신의 표현으로 완성

AI가 Moment를 추출한 뒤에 결과를 바로 저장하지 않고, 사용자가 한 번 더 확인하고 자신의 기록으로 완성하도록 설계했습니다.

- AI는 사용자가 작성한 내용 중 Moment에 해당하는 부분을 Highlight하고, Happy / Lucky 판단과 그 이유를 함께 제안
- 제안된 Moment와 Clover 유형은 Entry 작성 단계로 이어지지만, 사용자가 자연스럽게 수정하고 다시 선택할 수 있도록 설계
- 캐릭터 말풍선 안내 문구를 통해 사용자가 자신의 표현으로 기록을 완성하도록 부드럽게 유도

즉, AI의 역할은 **Moment를 대신 기록하는 것이 아니라 발견의 시작점을 제공하는 것**으로 제한하고, 최종 기록에 대한 결정권은 사용자에게 남겼습니다.

### ③ 부담은 낮추고, Retention 유도는 Character Raising으로 설계

Survey n=100에서 Character Raising 경험자의 84%가 키우기 요소가 앱 선택에 영향을 줬다고 응답했으며, 주요 이유는 동기부여 및 보상과 재미였습니다. 이를 바탕으로 Clover Collection을 통한 Character Raising을 Retention 장치로 설계했습니다.

**Reward Structure**
- Happy Moment는 세잎 Clover, Lucky Moment는 네잎 Clover로 저장하되, 두 유형의 보상 가치에는 차이를 두지 않아 특정 경험을 억지로 찾도록 유도하지 않았습니다.

**Retention Loop**
- 연속 기록 여부와 관계없이 누적 3일 기록 시, Home에서 Clovy 주변에 나타나는 3개의 Clover를 수집하는 Collection Event를 통해 기록의 보상을 시각적으로 경험하도록 설계했습니다.
- 모은 Clover를 Clovy에게 먹여 캐릭터를 성장시키는 구조로 연결해, 기록이 누적될수록 다시 돌아올 이유를 만들었습니다.

**Low-pressure UX**
- 하루를 쉬어도 3일 누적 기록 초기화나 Penalty가 없도록 해 언제든 부담 없이 다시 기록할 수 있도록 했습니다.
- AI 자체를 Clovy 캐릭터로 설정하고, 안내 및 피드백 문구도 사용자를 평가하거나 압박하지 않는 Low-pressure Tone으로 일관되게 설계했습니다.

---

## 3. 지표

출시 전 Event Logging을 구축하고, 실제 사용자 행동 데이터를 통해 아래 세 가지를 확인하도록 설계했습니다.

### ① AI가 실제로 Moment 발견을 돕는가?

- **Moment Extraction 성공률**
- 추출 성공까지 필요한 **평균 Follow-up 횟수 및 0~4회별 성공 비율**
- Follow-up 또는 일일 AI 사용량 소진으로 인한 **Extraction 실패 비율**

→ AI가 한 번에 Moment를 잘 발견하는지, 반복적인 대화가 필요한지, 사용량 제한이 발견 경험을 방해하는지 확인

### ② 사용자는 AI가 발견한 Moment를 그대로 받아들이는가?

- 추출된 Moment의 **그대로 적용 / 수정 후 적용 / 삭제 / 이탈 비율**
- 수정 발생 시 **Text / Clover 유형 / 둘 다 수정한 비율**

→ AI의 제안이 사용자 판단과 얼마나 일치하는지, 어떤 부분에서 사용자의 수정이 주로 발생하는지 확인

### ③ 실제 사용자는 어떤 방식으로 기록하는가?

- 일별 Direct / AI / Both 작성 방식 비율
- 저장된 Entry의 Direct / AI 작성 비율
- 사용자당 평균 일기 작성 횟수
- 사용자당 평균 App Open 횟수
- 하루 평균 AI 사용 횟수

→ 출시 초기에는 Direct와 AI Flow의 실제 활용 비중과 사용자별 기록·앱 사용 패턴을 파악

### 2차 Measurement 고도화

1차 모델에서는 출시를 지연시키지 않으면서 핵심 사용 패턴을 확인할 수 있는 범위로 Event Logging을 우선 구축했습니다.
실제 사용 데이터가 축적된 이후에는 Event Logging을 확장해 작성 방식과 반복 기록, 재방문의 관계까지 분석할 계획입니다.

- Direct / AI Flow별 Entry 저장 완료율
- 첫 기록 방식별 7일 내 추가 Entry 작성률
- Direct / AI / Both 사용자별 D7 재방문율
- 사용자별 주간 기록 일수 및 App Open 일수
- 첫 기록 이후 다음 기록까지의 소요 시간

→ 단순한 기능 사용량을 넘어, 어떤 작성 경험이 실제 Entry 저장과 이후 반복 기록 및 재방문으로 이어지는지 비교

---

## 4. 성과 및 결과

- iOS App Store 출시
- AI 품질 검증을 위해 **307개 Test Case** 수행
- Console 통과율 **93.1%**
- 실제 App Focused Case **2/6 → 6/6 개선**
- 출시 후 14일/20명의 행동 데이터를 분석해 재방문율 X%, 기록 작성률 Y%, AI 사용률 Z% 확인, [발견한 Insight/개선]


---

## 5. Contribution

1명의 Product Manager / Product Designer로 전체 Product를 담당하고,  
iOS Frontend Developer 1명, Backend / AI Developer 1명과 협업했습니다.

- Product Discovery 및 문제 정의
- Product Policy 및 User Flow 설계
- UX/UI Design
- AI Output Policy 및 Follow-up Rule 설계
- AI Test Case 설계 및 결과 분석
- Device QA 및 Release
- Event Logging 및 Measurement 설계
