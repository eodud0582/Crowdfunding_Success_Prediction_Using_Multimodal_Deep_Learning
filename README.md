# 딥러닝을 이용한 크라우드펀딩 성공 예측
## 멀티모달 딥러닝 기반 크라우드펀딩 성공 예측 모델 개발

![image](https://user-images.githubusercontent.com/38115693/156875818-86c3e4e1-31e9-47cb-ab3e-b3d321d0678c.png)

## 프로젝트 배경
- NGO, NPO, CBO, CSO, 사회적 기업, 소셜 벤처 등 운영 또는 프로그램/사업 수행 자금 및 재정 문제
- 특히 비영리적 성격이 강하거나 완전한 비영리인 경우 이러한 문제는 고질적
- 하지만 정부 지원, 재단 후원, 기업의 투자, 협력 사업 등을 통한 자금 지원을 얻는 것엔 한계나 어려움이 항상 있음
- 이에 대한 해결책으로 크라우드펀딩을 통한 모금
- **크라우드펀딩 성공을 미리 예측하는 것이 펀딩 성공에 큰 도움이 될 것으로 판단**

## 프로젝트 설명
- 세계 최대 크라우드펀딩 플랫폼 Kistarter 데이터 수집
  - 17만개 이상의 성공적인 펀드레이징, 1,700만명 이상의 후원자, 4조 8천억원의 총 모금액
  - 방대한 양의 데이터를 통해 다양한 인사이트를 얻을 수 있을 것으로 판단
- **펀딩 런칭 전(pre-launch)** 관련 요인/특성 데이터만 사용
  - 지금까지의 크라우드펀딩 예측 관련 연구나 논문들은 펀딩 런칭 후(post-launch)에 발생하는 요인, 결과 또는 역학(dynamics)을 분석한 펀딩 결과 예측이 대부분 (ex: 댓글, 답글, 소셜미디어/온라인 상의 전파, 파급력, 공유 횟수, 후원자 수 등)
  - 하지만 이러한 펀딩 런칭 후 발생하는 요인과 결과는 모금을 하는 대상이 그 결과를 만들어내거나 제어 할 수 없는 또는 한계가 큰 요인인 것이 대부분이며, 이러한 런칭 후 발생하는 요인을 이용한 결과 예측은 런칭 후 일정 시간이 지난 뒤에야 펀딩 결과를 예측을 할 수 있거나 시기적절하게 결과를 예측 할 수 없고 펀딩을 수정하거나 개선하는 것에도 어려움과 한계가 있음
  - 하지만 펀딩 런칭 전(pre-launch)과 관련된 요인들은 직접 설정과 제어를 할 수 있으며, 그리고 펀딩 런칭 전에 펀딩 성공/성공율을 미리 예측 할 수 있다면 무엇이 문제일지 고민하고 파악할 수 있고 성공율을 더 높이는 방향으로 펀딩 프로젝트를 수정/개선해 갈 수 있고, 이렇게 사전에 미리 잘 준비하고 퀄리티 있는 프로젝트를 만들 수 있다면 펀딩 성공율은 크게 증가할 것
  - 한 마디로, 펀딩을 런칭하기 전에 미리 펑딩에 성공 할 수 있는 펀딩 프로젝트를 만드는 것
- 탐색적 분석 및 딥러닝을 활용한 펀딩 성공 예측 모델링

## 기대 효과
- 성공 할 수 있는 또는 가능성이 큰 크라우드펀딩 프로젝트를 만들 수 있다면:
  - 대중에게 기업/기관 또는 개인의 일과 분야에 대해 알릴 수 있고 대중의 관심을 이끌어내거나 대중의 인식을 높일 수 있으며
  - 모금을 통해 필요한 자원/자금 또한 얻을 수 있음

## 데이터셋
- 메타 데이터(크라우드펀딩 상품 프로필 데이터)
  - 정형 데이터
  - 목표 모금액, 모금기간 등 펀딩에 대한 다양한 설정
- 이미지 데이터
  - 펀딩 프로젝트에 사용된 메인 사진
  - 웹사이트 메뉴나 펀딩 페이지 상에서 가장 먼저 눈에 보임
- 텍스트(text) 데이터
  - 펀딩 제목, 부제목(펀딩에 대한 간략한 설명글), 본문

## 기술 스택
- Python
- Google Clound Platform (GCP)

## 분석 방향
- 탐색적 분석 및 복합적/다각적 딥러닝 모델 구현
- 수집한 메타 데이터(정형데이터), 이미지 데이터, 텍스트 데이터 각각을 예측 모델링에 적합하게 전처리 및 가공
  - 단계
    1. 메타 데이터 처리
    2. 이미지 데이터 처리
    3. 텍스트 데이터 처리
- 그 세 처리 결과를 하나로 결합 후 딥러닝 모델에 학습시켜 모델링, 검증 및 평가
- 이후 웹어플리케이션으로 구현

## 프로젝트 현황
1. 메타 데이터 처리 - 1차 탐색 및 전처리
2. 메타 데이터 처리 - 모델링에 사용할 예측변수 EDA 및 2차 전처리
3. 이미지 데이터 처리 - 전이 학습 및 특성 추출
4. 텍스트 데이터 처리 - 데이터 수집/크롤링
5. 텍스트 데이터 분리 및 결합
6. 텍스트 데이터 처리 및 딥러닝 적용
7. **문제 발생 (해결 예정)**
    - 큰 데이터 사이즈로 지속적인 **메모리 오류** 발생
    - 문제 해결을 위한 시도
      - CPU/GPU 성능 업그레이드
      - 더 가벼운 모델 사용
      - 데이터 규모 축소 등

## 향후 과제
- 발생한 메모리 오류 문제 해결
  - 데이터 차원 축소해서 진행
  - 데이터 규모를 더 줄여서 시도
- 문제 해결 후, 처리된 메타, 이미지, 텍스트 데이터들을 결합하고 딥러닝 학습 및 모델링 진행
