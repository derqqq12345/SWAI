🔥 Real-Time Fire Alarm Automation System
객체 탐지와 LLM을 활용한 실시간 화재 경보 자동화 시스템

YOLO 기반 객체 탐지와 LLM 기반 상황 분석을 결합한
End-to-End 실시간 화재 감지 및 경보 자동화 시스템

🏆 2025 한국소프트웨어종합학술대회(KSC2025) 주니어 논문 발표 프로젝트

🚀 Overview

본 프로젝트는 실시간 화재 탐지 및 자동 경보 시스템 구축을 목표로 합니다.

🔍 Core Features
YOLOv11 기반 Fire / Smoke 객체 탐지
LLM 기반 상황 분석 및 경보 메시지 생성
실시간 추론 환경 구축 (FPS + 정확도 균형 고려)
Precision-Recall 균형 기반 모델 최적화

단순 탐지를 넘어,
실제 적용 환경에서 안정적으로 작동 가능한 AI 시스템 설계에 집중했습니다.

🏗 System Architecture
Input (Image / Video Stream)
        ↓
YOLOv11 Object Detection (Fire / Smoke)
        ↓
Detection Result Parsing
        ↓
LLM 기반 상황 분석
        ↓
자동 경보 메시지 생성 및 출력
👥 Team
Name	Role
류현정	Fire Detection AI Development
손경민	Backend / Frontend
김동환	Data Collection
류지우	Data Collection
SWAI 인재양성 프로젝트 팀 참여
KSC2025 학술대회 발표 프로젝트
🧠 Model Development Strategy
1️⃣ Baseline 구축
YOLOv11n 기반 baseline 모델 설계
Fire / Smoke 클래스 성능 편차 분석
mAP50, mAP50-95, Precision, Recall 기준 설정
2️⃣ 성능 개선 전략
Mosaic / MixUp 데이터 증강
하이퍼파라미터 튜닝
클래스별 정량 분석 기반 개선
Confidence Threshold 재설정
모델 사이즈 비교 (n / s / m)
3️⃣ 실전 적용 고려 요소
⚡ FPS (추론 속도) 평가
📊 Precision-Recall 균형 고려
단순 최고 mAP 모델이 아닌 일반화 성능 기반 모델 선정
📊 Performance Improvement
Metric	Baseline	Final Model
mAP50	0.87	0.93
Smoke Recall	0.85	0.89
Precision	-	0.93

False Positive 증가 없이 Recall을 개선하는 방향으로 최적화하였습니다.

🚧 Challenges & Solutions
🔹 클래스 불균형 문제

문제

Fire > Smoke 데이터 편향
다수 클래스 중심 학습 발생

해결

Mosaic / MixUp 증강 적용
클래스 간 경계 학습 강화
데이터 다양성 확보
🔹 Smoke 낮은 Recall 문제

문제

Smoke의 시각적 특징 모호
미탐지율 증가

해결

클래스별 성능 분리 분석
하이퍼파라미터 재설계
Confidence Threshold 조정
Precision-Recall 균형 기반 모델 선정
📈 Key Insights
성능 개선은 모델 변경이 아닌 데이터 이해에서 시작된다
단일 지표(mAP) 최적화는 실제 환경에서 위험하다
Precision-Recall 균형이 실전 시스템에서 핵심이다
모델 Capacity와 데이터 규모 간 균형 설계가 중요하다
🛠 Tech Stack
Python
PyTorch
YOLOv11
CUDA / GPU Training
LLM 기반 텍스트 생성 모델
Flask (API)
Web UI
📂 Project Structure
├── dataset/
├── models/
├── train.py
├── val.py
├── inference.py
├── llm_analysis.py
├── utils/
└── app/
🎯 Future Work
다양한 기상 환경 데이터 확장
Edge Device 최적화
모델 추가 경량화
멀티 클래스 확장 (가스, 폭발 등)
🔥 Conclusion

본 프로젝트는 객체 탐지와 LLM을 결합하여
실시간 환경에서 동작 가능한 AI 기반 화재 경보 시스템을 설계하고 구현한 사례입니다.

정량적 성능뿐 아니라, 실제 환경에서의 안정성과 일반화 성능을 고려한 모델 설계에 중점을 두었습니다.
