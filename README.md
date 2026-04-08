#🔥 Real-Time Fire Alarm Automation System
객체 탐지와 LLM을 활용한 실시간 화재 경보 자동화 시스템

YOLO 기반 객체 탐지와 LLM 기반 상황 분석을 결합한 End-to-End 화재 감지 및 경보 자동화 시스템
2025 한국소프트웨어종합학술대회(KSC2025) 주니어 논문 게재

📌 Overview

본 프로젝트는 실시간 화재 탐지 및 자동 경보 시스템을 구축하는 것을 목표로 합니다.

🔍 YOLOv11 기반 화재/연기 객체 탐지
🧠 LLM 기반 상황 분석 및 텍스트 경보 생성
⚡ 실시간 추론 환경 구축 (속도 + 정확도 균형 고려)
📊 Precision-Recall 균형 기반 모델 최적화

단순 탐지를 넘어, 실제 적용 환경에서 안정적으로 작동 가능한 AI 시스템 설계에 집중했습니다.

🏗 System Architecture
Input (Image / Video Stream)
        ↓
YOLOv11 Object Detection (Fire / Smoke)
        ↓
Detection Result Parsing
        ↓
LLM 기반 상황 분석 및 경보 메시지 생성
        ↓
자동 경보 출력 (UI / Alert System)
👥 Team & Role
Name	Role
류현정	👑 Team Leader / Fire Detection AI Development
손경민	Backend / Frontend
김동환	Data Collection
류지우	Data Collection
SWAI 인재양성 프로젝트 팀장
KSC2025 주니어 논문 1저자
🧠 Model Development Process
1️⃣ Baseline 구축
YOLOv11n 기반 baseline 모델 설계
Fire / Smoke 클래스 성능 편차 분석
mAP50, mAP50-95, Precision, Recall 기준 설정
2️⃣ 성능 개선 전략
데이터 증강 (Mosaic, MixUp)
하이퍼파라미터 튜닝
클래스별 정량 분석 기반 개선
임계값 재설정 (Confidence Threshold Optimization)
모델 사이즈 비교 (n / s / m)
3️⃣ 실제 환경 고려 요소
FPS (추론 속도) 평가
Precision-Recall 균형 고려
단순 최고 mAP 모델이 아닌 일반화 성능 기반 최종 모델 선정
📊 Performance Improvement
Metric	Baseline	Final Model
mAP50	0.87	0.93
Smoke Recall	0.85	0.89
Precision	-	0.93 안정화

📌 단순 수치 향상이 아닌,
False Positive 증가 없이 Recall을 개선하는 방향으로 최적화하였습니다.

🚧 Challenges & Solutions
🔹 1. 클래스 불균형 문제
Fire > Smoke 데이터 편향 발생
다수 클래스 중심 학습 문제

해결 방법

Mosaic / MixUp 증강 적용
클래스 간 경계 학습 강화
데이터 다양성 확보
🔹 2. Smoke 낮은 Recall 문제

Smoke는 경계가 모호하고 시각적 특징이 불분명하여 미탐지율이 높았습니다.

해결 방법

클래스별 성능 분리 분석
하이퍼파라미터 재설계
임계값 조정
Precision-Recall 균형 기반 모델 선정
📈 Key Insight

✔ 성능 개선은 모델 변경이 아니라 데이터 이해에서 시작된다
✔ 단일 지표(mAP) 최적화는 실제 환경에서 위험하다
✔ Precision-Recall 균형이 실전 시스템에서 핵심이다
✔ 모델 Capacity와 데이터 규모 간 균형 설계가 중요하다

🛠 Tech Stack
Python
PyTorch
YOLOv11
CUDA / GPU Training Environment
LLM 기반 텍스트 생성 모델
Flask (API)
Web UI
📂 Project Structure (Example)
├── dataset/
├── models/
├── train.py
├── val.py
├── inference.py
├── llm_analysis.py
├── utils/
└── app/
📄 Publication

📌 2025 한국소프트웨어종합학술대회 (KSC2025)
주니어 논문 부문 1저자 게재

객체 탐지와 LLM을 활용한 실시간 화재 경보 자동화 시스템

🎯 Future Work
다양한 기상 환경 데이터 추가 수집
Edge Device 최적화
모델 경량화 추가 실험
멀티 클래스 확장 (가스, 폭발 등)
🔥 Final Note

이 프로젝트는 단순한 객체 탐지를 넘어
실제 적용 가능한 AI 시스템을 설계하는 경험이었습니다.

성능은 숫자가 아니라
"현장에서 얼마나 안정적으로 작동하는가"로 판단해야 한다는 것을 배웠습니다.
