# ⚡ FTL 마스터: Senior Staff Firmware Engineer 편
> **High-Performance NAND Flash Translation Layer Architecture, Reliability & System Engineering**

SanDisk/Western Digital의 **Senior Staff Firmware Engineer** 포지션 준비 및 FTL 심화 학습을 위해 제작된 올인원 인터랙티브 학습 플랫폼입니다.

---

## 🌟 주요 특징 및 구성

### 1. 📖 체계적인 단계별 심화 학습
- **Tab 1. FTL 기초 및 핵심 (Core Foundations):** NAND 3대 물리적 한계, Out-of-Place Update, L2P 맵핑(Page vs Block vs Hybrid), 가비지 컬렉션(GC) & 쓰기 증폭률(WAF), 정적/동적 웨어 레벨링, 오버 프로비저닝(OP) 및 TRIM.
- **Tab 2. NAND 미디어 물리 계층 & 신뢰성 (Media Management):** 3D BiCS NAND(CTF)의 Vth 분포 왜곡(Data Retention, Read Disturb, Temperature Cross), 하드웨어 LDPC ECC와 FTL Dynamic Read Calibration (Read Retry / Moving Read / Read Reclaim), Open Block 관리 및 Sequential Wordline 제약, Lower-Page Corruption 방어, 런타임 배드 블록 관리(BBM).
- **Tab 3. 고성능 아키텍처 & 레이턴시 QoS (Architecture & QoS):** Demand-based FTL (DFTL) & NVMe HMB, Superblock 가상화 및 Internal Die-RAID (SanDisk Guard), Pseudo-SLC Caching & Direct Folding & Performance Cliff 방어, Program/Erase Suspend & Resume (Tail Latency 선점 제어), 서든 파워 오프(SPO Recovery - HW PLP vs SW Checkpoint & Journaling), 차세대 NVMe 표준(FDP & ZNS).
- **Tab 4. Senior Staff 면접 & 전략 (Interview & 18-Year Career Bridge):**
  - **김회원 님의 18년 임베디드 실적과 FTL 핵심 난제 1:1 매핑 표** (이종 멀티코어 경합 해소 ➔ FTL Multi-Core 파이프라인 스케줄링, 동적 할당 배제 정적 버퍼 풀링 ➔ DFTL 캐시 무단편화 설계, 40만 프레임 Aging 무결점 ➔ SPO 저널링 무결성, HW 가속기 레지스터 직접 제어 ➔ 온칩 Flash Controller 오프로딩).
  - **시니어 스태프 인터뷰 예상 질문 TOP 5 & 모범 답변 프레임**.
  - **실전 펌웨어 가혹 환경 테스트 설계** (SPO Power Injection, 고온 Aging) 및 버스 애널라이저(Teledyne LeCroy PCIe TLP), 인메모리 컴팩트 링 버퍼 트레이서 디버깅.

### 2. 🎮 인터랙티브 시뮬레이터 (Interactive Simulators)
- **① LBA-PBA Out-of-Place Mapping & GC Simulator:**
  - LBA(0~3)에 데이터를 직접 쓰면서 구 데이터의 무효화(Invalidation)와 새 페이지 할당 과정을 시각적으로 확인.
  - 블록 포화 시 가비지 컬렉션(GC) 발동 ➔ 유효 데이터 이사 ➔ 소거(Erase) ➔ 실시간 WAF 계산.
- **② Dynamic Read Calibration (Read Retry & Moving Read) Canvas Simulator:**
  - 셀 열화(Data Retention, Read Disturb, Temperature Cross)에 따른 Vth 가우시안 분포 왜곡 시각화.
  - Vref 오프셋 슬라이더를 직접 조절하여 LDPC 디코딩 성공 및 Read Reclaim 알림 트리거 체험.

### 3. 🎯 실전 모의고사 & 스마트 오답 가중치 시스템 (Mastery Test)
- 총 **32개 고품질 문항** (기초, 미디어 물리, 고성능 아키텍처, 시니어 면접/실무).
- 카테고리별 필터 및 10문제 단위 모의고사 세션.
- **스마트 오답 가중치 알고리즘:** 틀린 문제는 가중치가 증가하여 다음 세션에 집중 출제 (100% 마스터리 달성까지 반복 학습).
- **원클릭 개념 복습 링크:** 오답 발생 시 해당 개념이 있는 탭과 카드로 즉시 이동 및 2초간 펄스 하이라이트.
- 키보드 단축키 지원 (1, 2, 3, 4로 답안 선택, Space/Enter로 다음 문제).
- 다크모드 / 라이트모드 완벽 지원 및 반응형 UI (모바일/태블릿/PC 최적화).

---

## 🚀 GitHub Pages로 무료 배포(Publish)하는 방법

이 프로젝트는 외부 무거운 라이브러리 없이 독립적으로 실행되는 단일 HTML 애플리케이션으로, GitHub Pages에 올리면 언제 어디서나 스마트폰이나 태블릿으로 학습할 수 있습니다.

### 방법:
1. GitHub에서 새 저장소(Repository)를 생성합니다 (예: `ftl_master_interactive`).
2. 로컬 저장소를 GitHub에 푸시합니다:
   ```bash
   git add .
   git commit -m "feat: complete senior staff FTL master interactive app"
   git remote add origin https://github.com/<YOUR_GITHUB_ID>/ftl_master_interactive.git
   git branch -M main
   git push -u origin main
   ```
3. GitHub 저장소 페이지의 **Settings** ➔ **Pages**로 이동합니다.
4. **Build and deployment** 항목의 **Source**를 `Deploy from a branch`로 선택하고, Branch를 `main` / `/(root)`로 지정한 후 **Save**를 누릅니다.
5. 약 1분 후 제공되는 URL(예: `https://<YOUR_GITHUB_ID>.github.io/ftl_master_interactive/`)로 접속하면 전 세계 어디서든 바로 학습할 수 있습니다!

---

## 💻 로컬에서 바로 실행하기
별도의 웹 서버 설치 없이 브라우저에서 `index.html` 파일을 더블 클릭하여 열면 모든 기능이 100% 오프라인으로 완벽 동작합니다.
