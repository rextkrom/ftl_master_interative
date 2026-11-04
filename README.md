# ⚡ Flash Memory & FTL Tech Suite: Senior Staff Firmware Engineer 편
> **SanDisk & Western Digital BiCS 3D NAND & High-Performance FTL Architecture Master Platform**

SanDisk/Western Digital의 **Senior Staff Firmware Engineer** 포지션 준비 및 스토리지 하드웨어/펌웨어 심화 학습을 위해 제작된 올인원 인터랙티브 기술 학습 플랫폼입니다.

---

## 🌐 GitHub Pages URL 접근 안내

GitHub Pages에 배포되면 아래의 모든 페이지에 전 세계 어디서든 모바일, 태블릿, PC로 직접 접속하실 수 있습니다:

1. **통합 포털 홈:**  
   👉 [https://rextkrom.github.io/ftl_master_interative/](https://rextkrom.github.io/ftl_master_interative/) (또는 `/index.html`)  
   - NAND Flash 편과 FTL 편을 한눈에 조망하고 선택하여 입장할 수 있는 메인 대시보드 및 권장 로드맵 제공.

2. **🔬 1편: NAND Flash 마스터 편:**  
   👉 [https://rextkrom.github.io/ftl_master_interative/nand.html](https://rextkrom.github.io/ftl_master_interative/nand.html)  
   - 셀 물리(CTF vs FG), 양자 FN 터널링, 직렬 스트링 도통 메커니즘, SLC~QLC 문턱 전압(Vth) 제어, ISPP 계단식 펄스, 3D BiCS 다이 아키텍처(CuA/PUC/CBA), Toggle DDR 5.0 / ONFI 5.1 고속 버스 프로토콜, 노이즈 & 신뢰성(Retention, Read Disturb, Self-Boosting, SILC), 낸드 특성화(Shmoo Plot, RBER 모델링, FMC 시퀀서), **2종 인터랙티브 시뮬레이터**, **28문항 실전 모의고사**.

3. **⚡ 2편: FTL 마스터 편:**  
   👉 [https://rextkrom.github.io/ftl_master_interative/ftl.html](https://rextkrom.github.io/ftl_master_interative/ftl.html)  
   - Out-of-Place L2P 맵핑, 가비지 컬렉션(GC) & WAF 최소화, 동적/정적 웨어 레벨링, OP & TRIM, DFTL 캐시 스왑 & NVMe HMB, Superblock 스트라이핑 병렬화, Internal Die-RAID(SanDisk Guard XOR 패리티 복원), Pseudo-SLC Caching & Folding Cliff 방어 피드백 루프, Erase Suspend 선점 QoS, 서든 파워 오프(SPO Recovery: HW PLP vs SW 저널링), 차세대 FDP/ZNS, **김회원 님의 18년 임베디드 이력 1:1 매핑 표 & 인터뷰 TOP 5 모범 답변**, **2종 인터랙티브 시뮬레이터**, **32문항 실전 모의고사**.

---

## 🌟 핵심 시스템 특징

### 🎮 인터랙티브 시뮬레이터 (총 4종)
- **NAND Flash 편:**
  - ① **SLC ~ QLC 문턱 전압(Vth) 분포 & 노이즈 마진 시뮬레이터**: 셀 레벨 전환 시 가우시안 피크 렌더링 및 P/E Cycle 노화에 따른 상태 중첩(Vth Overlap) 시각화.
  - ② **Toggle/ONFI Flash Bus 신호 타이밍 파형 시뮬레이터**: Page Read(`00h-30h`), Page Program(`80h-10h`), Block Erase(`60h-D0h`)의 CLE, ALE, WE#, RE#, R/B#, DQ 디지털 버스 파형 실시간 렌더링.
- **FTL 편:**
  - ① **LBA-PBA Out-of-Place Mapping & GC Simulator**: 직접 데이터 쓰기, Valid/Invalid 마킹, GC 트리거 및 실시간 WAF 계산.
  - ② **Dynamic Read Calibration (Read Retry & Moving Read) 시뮬레이터**: Vth 왜곡 시 FTL Vref 오프셋 슬라이더 제어로 비트 에러 복구 및 Read Reclaim 알림 체험.

### 🎯 스마트 실전 모의고사 (총 60문항: NAND 28문항 + FTL 32문항)
- 세션당 10문제씩 가중치 기반 랜덤 출제.
- **스마트 오답 가중치 알고리즘:** 틀린 문제는 가중치가 상승하여 다음 모의고사 시 집중 우선 출제 (100% 마스터리 달성까지 반복 학습).
- **원클릭 개념 복습 링크:** 오답 발생 시 해당 개념이 수록된 탭과 카드로 즉시 이동 및 2초간 펄스 하이라이트 애니메이션.
- 키보드 숫자키(`1`, `2`, `3`, `4`) 및 `Space`/`Enter` 단축키 지원.

---

## 🚀 GitHub Pages 배포 방법

1. 변경된 모든 파일을 커밋하고 GitHub에 푸시합니다:
   ```bash
   git add .
   git commit -m "feat: complete dual master suite (index, nand, ftl)"
   git push origin main
   ```
2. GitHub 저장소의 **Settings** ➔ **Pages**로 이동합니다.
3. **Source**를 `Deploy from a branch`로 선택하고, **Branch**를 `main` / `/(root)`로 지정한 뒤 **Save**를 누릅니다.
4. 약 1분 후 제공되는 GitHub Pages URL([https://rextkrom.github.io/ftl_master_interative/](https://rextkrom.github.io/ftl_master_interative/))로 접속하면 모든 문서가 완벽하게 서비스됩니다.

---

## 💻 로컬에서 바로 실행하기
별도의 웹 서버나 설치 없이 브라우저에서 `index.html`, `nand.html`, `ftl.html` 중 원하는 파일을 더블 클릭하여 열면 오프라인에서도 모든 기능이 100% 정상 작동합니다.
