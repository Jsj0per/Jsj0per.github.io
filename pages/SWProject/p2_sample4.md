---
title: 꼬마선장 에코
keywords: sample
summary: "난독증으로 어려움을 겪는 학생들을 위한 난독증 증상 개선 목적의 교육 사이트 제작."
sidebar: SWProject_sidebar
permalink: p2_sample4.html
folder: product2
---

# 주의 사항

SSAFY 프로젝트는 보안 관계상 모든 소스코드 파일 열람이 불가능합니다.  
열람이 필요하실 경우 저에게 연락한 뒤 제가 SSAFY를 통하여 소스코드 열람을 허가를 받은 뒤 공개가 가능합니다.  

---

# 🚢 Captain Echo (꼬마선장 에코)

> **AI 멀티 에이전트가 만드는 맞춤형 난독증 학습 여정**
> CrewAI 기반 3+1 에이전트 협업으로 아동 개개인에게 최적화된 학습 커리큘럼을 자동 생성합니다.

<iframe width="560" height="315" src="https://www.youtube.com/embed/9ht3jnHnNjM?si=fmY3Ad1Le32VDQEs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>  

<br />

## 📄 목차
- [📄 목차](#-목차)
- [✨ 프로젝트 소개](#-프로젝트-소개)
  - [기획 배경](#기획-배경)
  - [서비스 개요](#서비스-개요)
- [🤖 핵심 차별점: AI 멀티 에이전트 시스템](#-핵심-차별점-ai-멀티-에이전트-시스템)
- [🚀 주요 기능](#-주요-기능)
  - [학생용 기능](#학생용-기능)
  - [보호자용 기능](#보호자용-기능)
- [⚙️ 기술 스택](#️-기술-스택)
  - [Backend](#backend)
  - [Frontend](#frontend)
  - [AI Service](#ai-service)
  - [Infrastructure & DevOps](#infrastructure--devops)
- [📅 개발 기간](#-개발-기간)

<br />

---

<br />

## ✨ 프로젝트 소개

### 기획 배경

**난독증(Dyslexia)**은 지능이나 학습 의욕과 무관하게 읽기와 쓰기에 어려움을 겪는 **음운인식 장애**입니다.
- 국내 초등학생의 **약 5-10%**가 난독증으로 추정됩니다
- 조기 발견 및 개입 시 **80% 이상 개선 가능**하지만, 개인별 맞춤 학습 콘텐츠 부족이 문제입니다
- 기존 획일적인 학습 교재는 **아동의 관심사, 현재 수준, 음소 혼동 패턴**을 반영하지 못합니다

### 서비스 개요

**Captain Echo**는 AI 멀티 에이전트가 아동의 학습 데이터를 분석하여 **매주 자동으로 맞춤 커리큘럼과 문제를 생성**하는 난독증 학습 플랫폼입니다.

- **개발 기간**: 2025.10.10 ~ 2025.11.20 (6주)
- **팀 구성**: 6명 (Backend 2, Frontend 2, AI 1, Infra 1)
- **핵심 기술**: CrewAI 멀티 에이전트 시스템, Spring Boot, React, FastAPI

**주요 특징**:
- 🎯 **개인 맞춤형 학습**: 초기 진단으로 음소 혼동 패턴 분석 후 약점 집중 학습
- 🤖 **AI 에이전트 협업**: 학습전문가·심리전문가·학부모대표 에이전트가 토론하여 최적 커리큘럼 생성
- 🎮 **게임화된 학습**: 모험 컨셉의 4가지 유형 학습 문제 (음소 맞추기, 빈칸 채우기, 단어 맞추기, 읽기 평가)
- 🔄 **자동 적응형 난이도**: 주간 정답률 분석 후 자동으로 레벨 조정
- 📊 **보호자 대시보드**: 학습 진행 상황, 오답 패턴, AI 생성 주간 리포트 제공

<br />

---

<br />

## 🤖 핵심 차별점: AI 멀티 에이전트 시스템

Captain Echo의 가장 큰 기술적 차별점은 **CrewAI 기반 멀티 에이전트 협업 시스템**입니다.

### 🎭 4-Agent 협업 구조

```
┌─────────────────────────────────────────────────────────────┐
│                    Manager Agent (조율자)                     │
│           GPT-4o 기반 최종 의사결정 및 품질 검증              │
└────────────────────┬────────────────────────────────────────┘
                     │ 조율 및 합의 도출
        ┌────────────┼────────────┐
        ↓            ↓            ↓
┌──────────────┐ ┌──────────────┐ ┌──────────────┐
│ Academic     │ │ Wellbeing    │ │ Parent       │
│ Agent        │ │ Agent        │ │ Agent        │
├──────────────┤ ├──────────────┤ ├──────────────┤
│ 학습 전문가   │ │ 심리 전문가   │ │ 학부모 대표   │
│              │ │              │ │              │
│• 음소 혼동    │ │• 인지 부하    │ │• 보호자 목표  │
│  패턴 분석    │ │  모니터링     │ │  반영         │
│• 난이도 조정  │ │• 자신감 관리  │ │• 학습량 균형  │
│• 학습 효율    │ │• 학습 동기    │ │• 실용성 검증  │
│  최적화       │ │  향상         │ │              │
└──────────────┘ └──────────────┘ └──────────────┘
        ↓            ↓            ↓
        └────────────┼────────────┘
                     ↓
          📋 맞춤형 주간 커리큘럼 생성
    (레벨, 문제 유형, 목표 음소, 학습 목표)
```

### 🔄 동작 원리

1. **데이터 수집**: 학생의 주간 학습 데이터 (정답률, 오답 패턴, 소요 시간, 현재 레벨)
2. **에이전트 토론** (Hierarchical Process):
   - Academic Agent: "ㄱ-ㄲ 혼동률 65% → 레벨 3 유지하며 집중 학습 필요"
   - Wellbeing Agent: "주간 정답률 45% → 자신감 저하 우려, 쉬운 문제 30% 포함"
   - Parent Agent: "보호자 목표: 약점 보완 → 혼동 음소 중심 구성 동의, 학습량 적정성 확인"
   - Manager Agent: "레벨 3, ㄱ-ㄲ 집중(60%), 복습(30%), 신규(10%) 배분으로 결정"
3. **커리큘럼 생성**: 에이전트 합의 결과를 JSON으로 구조화
4. **문제 자동 생성**: 커리큘럼 기반으로 LLM(GPT-4o/Gemini)이 실제 학습 문제 생성
5. **주간 재생성**: 매주 일요일 23:00 자동 실행 (APScheduler)

### 🎯 실제 적용 효과

- ✅ **개인화 정확도**: 음소별 혼동률 패턴 반영으로 학습 효율 ↑
- ✅ **학습 지속성**: 심리 전문가 에이전트의 난이도 조절로 중도 포기율 ↓
- ✅ **보호자 신뢰**: 투명한 의사결정 과정 제공으로 만족도 ↑

<br />

---

<br />

## 🚀 주요 기능

### 학생용 기능

#### 1️⃣ 초기 진단 시스템
- 40개 문항으로 **자모 혼동 패턴** 정밀 분석 (예: ㄱ-ㄲ, ㅓ-ㅕ)
- 진단 결과 기반 **개인 맞춤 학습 프로필** 생성
- AI가 약점 음소 우선순위 결정

#### 2️⃣ 4가지 유형의 학습 모험
- **Type 1: 음소 맞추기** - 단어 듣고 정확한 자음/모음 선택
- **Type 2: 빈칸 채우기** - 문장 맥락에서 알맞은 음소 채우기
- **Type 3: 단어-이미지 매칭** - 그림 보고 정확한 단어 선택
- **Type 4: 읽기 평가 (STT)** - 음성 인식으로 발음 정확도 평가

#### 3️⃣ 6단계 레벨 시스템
```
Level 1: 기본 자모 (ㄱ, ㄴ, ㄷ)
Level 2: 쌍자음 (ㄲ, ㄸ, ㅃ)
Level 3: 복잡한 모음 (ㅘ, ㅙ, ㅝ)
Level 4: 받침 조합
Level 5: 복합 단어
Level 6: 문장 독해
```
- 주간 정답률 70% 이상 시 자동 레벨업
- 50% 미만 시 레벨 유지 및 복습 강화

#### 4️⃣ 관심사 기반 학습
- 회원가입 시 관심사 선택 (동물, 스포츠, 음식, 자연 등)
- AI가 관심사 키워드로 문제 생성 → 학습 몰입도 ↑
  - 예: 동물 좋아하는 아동 → "강아지", "고양이" 단어 문제

#### 5️⃣ 보상 시스템 (앵무새 상점)
- 학습 완료 시 가상 화폐 지급
- 앵무새 꾸미기 아이템 구매
- 학습 동기 부여 및 지속성 확보

<br />

### 보호자용 기능

#### 1️⃣ 학생 관리
- 최대 **2명의 자녀** 프로필 관리
- PIN 번호로 학생 프로필 보호
- 자녀별 독립적인 학습 데이터 관리

#### 2️⃣ 학습 목표 설정
보호자가 자녀의 학습 방향을 직접 선택:
- **약점 보완**: 틀린 음소 집중 학습
- **자신감 향상**: 적정 난이도 유지로 성취감 제공
- **난이도 상승**: 도전적 문제로 빠른 성장

→ Parent Agent가 이 목표를 커리큘럼 생성에 반영

#### 3️⃣ AI 생성 주간 리포트
매주 AI가 자동 생성하는 상세 리포트:
- 📈 **학습 성과**: 정답률, 학습 시간, 연속 출석일
- 🎯 **약점 분석**: 음소별 정답률, 문제 유형별 성과
- 📋 **다음 주 계획**: AI 에이전트가 결정한 학습 목표 및 근거
- 💡 **학습 제안**: 가정에서 할 수 있는 추가 활동

#### 4️⃣ 상세 분석 대시보드
- 📊 **정답률 추이 그래프** (일간/주간/월간)
- 🔍 **오답 패턴 분석** (자주 틀리는 음소 조합)
- ⏱️ **학습 시간 통계**
- 🏆 **성취 배지 및 마일스톤**

---

<br />

## ⚙️ 기술 스택

### Backend
<img src="https://img.shields.io/badge/Java_21-007396?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot_3.5.7-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/> <img src="https://img.shields.io/badge/AWS_S3-569A31?style=flat-square&logo=amazons3&logoColor=white"/>

- **Framework**: Spring Boot 3.5.7 (Java 21)
- **Database**: PostgreSQL (JPA/Hibernate ORM)
- **Cache**: Redis (세션 관리, Rate Limiting)
- **Authentication**:
  - OAuth2 (Google Login)
  - JWT Token (Access + Refresh)
- **Storage**: AWS S3 (음성 파일, 이미지)
- **Email**: Spring Mail (SMTP)
- **Monitoring**:
  - Spring Boot Actuator
  - Prometheus Metrics
  - Grafana Dashboard
- **API Docs**: SpringDoc OpenAPI 3.0 (Swagger UI)
- **Libraries**:
  - Lombok (보일러플레이트 제거)
  - MapStruct (DTO 변환)

### Frontend
<img src="https://img.shields.io/badge/React_18-61DAFB?style=flat-square&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white"/> <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white"/> <img src="https://img.shields.io/badge/Zustand-000000?style=flat-square&logo=zustand&logoColor=white"/>

- **Framework**: React 18.2 + TypeScript 4.9
- **Build Tool**: Vite 5.0 (빠른 HMR)
- **Routing**: React Router 6.30
- **State Management**:
  - Zustand 4.4 (전역 상태)
  - TanStack React Query 5.8 (서버 상태)
- **Form Handling**: React Hook Form + Zod (스키마 검증)
- **Styling**:
  - Tailwind CSS 4.1
  - Framer Motion (애니메이션)
- **HTTP Client**: Axios + React Query
- **Authentication**: @react-oauth/google
- **Korean Text**: hangul-js (자모 분리/조합)
- **Charts**: Recharts (학습 분석 그래프)
- **Testing**: Vitest + React Testing Library

### AI Service
<img src="https://img.shields.io/badge/Python_3.11-3776AB?style=flat-square&logo=python&logoColor=white"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/CrewAI-FF6B6B?style=flat-square&logo=ai&logoColor=white"/> <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white"/> <img src="https://img.shields.io/badge/ChromaDB-FF6B6B?style=flat-square&logo=database&logoColor=white"/>

- **Framework**: FastAPI 0.120
- **AI Orchestration**: **CrewAI 1.3** (Hierarchical Multi-Agent)
- **LLM**:
  - OpenAI GPT-4o (메인)
  - Google Gemini 1.5 Pro (보조)
- **Vector Database**:
  - ChromaDB (문제 임베딩)
  - LanceDB (성능 최적화)
- **Database ORM**: SQLAlchemy 2.0
- **Scheduler**: APScheduler (주간 커리큘럼 생성)
- **ML Libraries**:
  - tiktoken (토큰 계산)
  - instructor (구조화된 LLM 출력)
  - tokenizers (텍스트 전처리)
- **Document Processing**:
  - pdfplumber (PDF 파싱)
  - python-docx (DOCX 파싱)
  - pytube (유튜브 자막 추출)
- **Cloud Storage**: boto3 (AWS S3)
- **Audio**: OpenAI Whisper API (STT)

### Infrastructure & DevOps
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/> <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white"/> <img src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white"/> <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white"/> <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white"/>

- **Containerization**:
  - Docker 24.x
  - Docker Compose (멀티 컨테이너 오케스트레이션)
- **Web Server**:
  - Nginx 1.25 (리버스 프록시)
  - CloudFlare SSL (Origin Certificate)
- **CI/CD**:
  - Jenkins 2.x (자동 빌드/배포)
  - GitLab Webhook 연동
  - develop 브랜치 → EC2 자동 배포
- **Monitoring**:
  - Prometheus (메트릭 수집)
  - Grafana (대시보드 시각화)
  - Node Exporter (시스템 메트릭)
- **Database**:
  - PostgreSQL 15 (커스텀 init 스크립트)
  - Redis 7.x
- **Cloud**: AWS EC2 (Ubuntu 22.04)

<br />

---

<br />

## 📅 개발 기간

**2025.10.10 ~ 2025.11.20** (6주)

- **Week 1-2**: 기획, 요구사항 분석, 기술 스택 선정
- **Week 3**: 백엔드 API 개발, AI 에이전트 프로토타입
- **Week 4**: 프론트엔드 UI/UX 구현, AI 서비스 연동
- **Week 5**: 통합 테스트, 버그 픽스, 성능 최적화
- **Week 6**: 최종 QA, 문서화, 배포

<br />

---

<br />

<div align="center">

**Captain Echo**는 난독증 아동과 보호자를 위한 진심 어린 기술 프로젝트입니다.
모든 아이들이 읽기의 즐거움을 느낄 수 있기를 바랍니다. 📚✨

</div>


---

## 참가 팀원

* 김XX(팀장, AI 기능 구현)
* 박XX(인프라, 서버, 프론트엔드 담당)
* 황XX(백엔드 구현 담당)
* 공XX(백엔드 구현 담당)
* 김XX(프론트엔드 담당)
* 정승재(프론트엔드 담당)

## 해당 프로젝트 기여내역

저는 해당 프로젝트에서 프론트엔드 파트를 담당하였습니다.  

로그인 전 메인 페이지, 소개 페이지, Auth 페이지, 프로필 선택, 학생 대시보드 구현을 담당했으며,  
전체적인 디자인, UI/UX를 다른 프론트엔드 담당들과 공동 분담하여 수행했습니다.  

---
