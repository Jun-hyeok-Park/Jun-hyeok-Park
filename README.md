![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=10&height=200&section=header&text=JUNHYEOK's%20GITHUB&fontSize=50&animation=twinkling&fontAlign=68&fontAlignY=36)

안전성과 효율성을 최우선으로 생각하는 자동차 임베디드 소프트웨어 개발자입니다. 
AUTOSAR 아키텍처와 ISO 26262 표준에 대한 이해를 바탕으로 신뢰성 높은 차량용 소프트웨어를 개발하는 것을 목표로 합니다.

**Embedded Software Designer | Developer** Konkuk Univ. (2017.03 ~ 2023.08)  
Bachelor’s Degree in Electrical and Electronic Engineering  

<a href="mailto:joonhyeoki@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=Gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/jun-hyeok-park-31b8a5293/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=LinkedIn&logoColor=white"></a>

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=wnsgur07)](https://solved.ac/ce_won/)
![mazandi profile](http://mazandi.herokuapp.com/api?handle=wnsgur07&theme=dark)
---

<table border="0" cellpadding="0" cellspacing="0">
  <tr>
    <td>
      <a href="https://git.io/streak-stats">
        <img src="https://streak-stats.demolab.com/?user=Jun-hyeok-Park&theme=dracula" alt="GitHub Streak"/>
      </a>
    </td>
    <td>
      <img src="https://github-readme-stats.vercel.app/api?username=Jun-hyeok-Park&show_icons=true&theme=dracula" alt="Jun-hyeok-Park's GitHub stats"/>
    </td>
  </tr>
</table>

[![Jun-hyeok-Park's github activity graph](https://github-readme-activity-graph.vercel.app/graph?username=Jun-hyeok-Park&custom_title=Jun-hyeok-Park's%20Activity%20Graph&hide_border=true&theme=react-dark)](https://github.com/ashutosh00710/github-readme-activity-graph)

---

## 🎓 Education & Training

### **현대오토에버 임베디드 모빌리티 SW 전문가 양성과정 (1,000시간)**
**교육 기간:** 2025년 4월 ~ 2025년 11월

현업 수준의 실무 역량 확보를 목표로, 1,000시간 동안 차량용 임베디드 SW 개발의 전 과정을 체계적으로 이수했습니다.
- **AUTOSAR 표준 플랫폼:** Mobilgene을 활용한 BSW, ASW, RTE End-to-End 개발 실무
- **실시간 시스템(RTOS):** Free-RTOS, OSEK(ERIKA3) 기반 Task 설계 및 MCU 펌웨어 프로그래밍
- **차량 네트워크:** CAN/FD, Ethernet 기반 통신 프로토콜(SomeIP, DoIP) 설계 및 구현
- **보안 및 OTA:** AES, RSA, TLS 기반 Secure OTA 및 Firmware A/B Partition 업데이트 시스템 구축
- **개발 프로세스:** A-SPICE, ISO 26262 표준 기반 요구사항 분석, 설계, 검증 프로세스 수행

---

## 📂 Projects

### 차량용 임베디드 SW 개발 프로젝트 (Team Lead)

**기간:** 2025.07 ~ 2025.08  
**역할:** 팀장 / 임베디드 SW 개발(원격주행, 긴급제동, 전방충돌경고, BSW 일부)  
**환경:**
- MCU: Infineon TC375 (Bare-metal)
- 언어: C, Python(pynput)
- 통신: CAN, UART(Bluetooth HC-06)
- Sensor/Actuator: ToF, 초음파, DC 모터, LED, Buzzer
- Tool: AURIX Dev Studio, UDE, Jira, Confluence, GitHub
- 테스트: Confluence 기반 TC 문서화, Doxygen & Lizard 기반 구조 분석  

<br />**[프로젝트 개요]**

4WD RC카 플랫폼을 기반으로 원격 주행, 긴급제동(AEB), 자율주차 등 차량 기본 기능을 SYS → SWE → 테스트 케이스의 흐름으로 A-SPICE 프로세스에 따라 설계·구현한 임베디드 SW 프로젝트.  
주행 제어, 센서 기반 안전 기능, 사용자 인터페이스 등 차량 핵심 기능을 하위 드라이버(BSW)부터 상위 제어로직(ASW)까지 직접 구현함.  

<br />**[담당 업무 및 주요 구현 내용]**

**1) 요구사항 분석 및 SW 아키텍처 설계**
- Confluence 기반으로 SYS 요구사항 → SWE 요구사항 → TC까지 End-to-End 체계화
- 6개 기능군(원격주행, 긴급제동, 자율주차,전방충돌경고, 방향지시등, 암호기반시동) 총 40+ 요구사항 명세
- 각 기능의 입력/출력·상태 플래그·인터페이스 설계
- 전체 FSM(IDLE → DRIVE → EMERGENCY_STOP → AUTO_PARK) 설계 및 상태 전이 정의

**2) BSW 개발**
- UART(Bluetooth HC-06) 초기화 및 수신 인터럽트 처리
- Motor(PWM): 채널 A/B 기반 4WD 제어, 듀티 변경 로직, 단계 감속 로직 구현
- ToF 센서(CAN) 인터럽트 기반 거리 데이터 수신
- LED/Buzzer 제어(GPT 기반): 방향지시등, 비상등, 주차 완료 표시, FCW 경고음

**3) 원격 주행 기능 개발**
- pynput 기반 키보드 입력 → UART 명령 수신 처리
- 전진·후진·좌회전·우회전·대각 이동 등 8방향 제어
- 방향지시등 연동
- 키 입력 미수신 시 부드러운 감속·정지 구현

**4) AEB(긴급제동) + FCW(전방 충돌 경고)**
- ToF 기반 전방 거리 실시간 측정
- 80cm 이하 접근 시 감속, 35cm 이하 접근 시 즉시 정지(AEB)
- AEB 동안 전진 입력 차단, 후진 후 안전거리 확보 시 자동 해제
- FCW: 경고음 2회 + 전방 비상등 깜빡임
- 장애물과의 정지 정확도 10cm ±1cm

<br />**[테스트 및 검증 활동]**
- 테스트 케이스(TC_SWE_XX) 40여 개 작성 및 Confluence 기록
- UART, Motor, Sensor 모듈 단위테스트 수행
- Doxygen + Graphviz로 헤더 순환 의존성 분석
- Lizard 기반 순환복잡도 분석 및 코드 리팩토링
- 실제 RC카를 통한 통합 테스트 및 FSM 기반 시나리오 검증 주도

<br />**[성과 및 결과]**
- AEB 정지 거리 오차 ±1cm 이내 달성
- 요구사항–테스트케이스 추적률 100% 유지
- FSM 기반 통합 후 비정상 상태 전이 0건
- 전체 24개 모듈에서 순환 의존성 0건 유지
- 기획–설계–구현–테스트 전 과정에서 팀장으로서 일정/품질 관리 수행

#### **Tech Stack**
<img src="https://img.shields.io/badge/c-A8B9CC.svg?style=for-the-badge&logo=c&logoColor=white"> <img src="https://img.shields.io/badge/aurix-F37321.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/git-%23F05032.svg?style=for-the-badge&logo=git&logoColor=white"> <img src="https://img.shields.io/badge/github-%23181717.svg?style=for-the-badge&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/jira-%230052CC.svg?style=for-the-badge&logo=jira&logoColor=white"> <img src="https://img.shields.io/badge/confluence-%23172B4D.svg?style=for-the-badge&logo=confluence&logoColor=white"> <img src="https://img.shields.io/badge/autosar-E44D26.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/a--spice-C82333.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/iso--26262-D9534F.svg?style=for-the-badge&logoColor=white">

---

### 차량용 통신시스템 구현 프로젝트 (Team Lead)

**기간:** 2025.09 ~ 2025.10  
**역할:** 팀장 / SOME/IP 기반 SOA 설계·구현 / 차량 제어 GUI 개발  
**환경:**
- 상위 제어기: Raspberry Pi 4
- 하위 제어기: Infineon TC375
- 상위 통신: SOME/IP(SOA) & DoIP(진단/OTA)
- 하위 통신 : CAN(SOA) & UDS(진단/OTA)
- 언어: C, C++, Python
- Tool: vsomeip, Qt6, AURIX Dev Studio, UDE, Jira, Confluence, GitHub

<br />**[프로젝트 개요]**

1차 프로젝트에서 구현한 원격 주행, 긴급제동(AEB), 자율주차, 암호기반 시동 기능을 SDV 개념에 맞추어 SOA(Service-Oriented Architecture) 기반의 Ethernet(SOME/IP)–CAN Gateway 아키텍처로 재구성한 프로젝트.  
상위 제어 영역은 Ethernet(SOME/IP, DoIP), 하위 제어 영역은 CAN(SOA), UDS(진단/OTA)로 구분하여 실차 구조(Ethernet 기반 서비스·CAN 기반 ECU 제어)를 모델링함.  
프로젝트 전체 범위에는 차량 제어(SOME/IP), 차량 상태 피드백(SOME/IP), 진단(UDS/DoIP), OTA 업데이트가 모두 포함되며,  
이 중 SOME/IP 기반 제어·상태 서비스와 Gateway, Qt6 GUI 개발을 직접 담당하여 하위 ECU(TC375)와 상위 제어기 간 양방향 통신을 서비스 기반 구조로 완성하였다.  

<br />**[담당 업무 및 주요 구현 내용]**

**1) SOME/IP 기반 SOA 아키텍처 설계 및 구현**
- 프로젝트 요구사항 “Ethernet 기반 서비스 지향 통신 적용(SOME/IP, DDS 등)” 충족을 위해 vsomeip 선택 후 SOME/IP 서비스 구조 직접 설계
- Control(Request/Response), Status(Publish/Subscribe) 2개 서비스 정의
- veh_control_service: 방향/속도/AEB/자율주차/인증
- veh_status_service: ToF 거리, AEB 상태, 인증 결과, 주차 단계
- WSL 환경에서 멀티캐스트 미지원으로 SD 실패 문제 발생 → 직접 분석 후 Client RPi 추가하여 PC–ClientRPi–ServerRPi 구조로 재설계

**2) Ethernet ↔ CAN Gateway 설계 및 구현**
- SOME/IP payload ↔ CAN 8-byte format을 직접 정의
    - Byte0 = command type / status type
    - Byte1~7 = parameter
- 전체 통신 흐름 구현
    - PC GUI → SOME/IP → Server RPi → CAN → TC375 → Motor/Sensor
    - TC375 status → CAN → Server RPi → SOME/IP → PC GUI

**3) 서비스 기반 기능 재설계 (SWE 단위 재편성)**
- 1차 프로젝트 기능을 서비스 단위로 재정의하고 프로토콜 설계
    - 방향 제어(0x01), 속도 제어(0x02), AEB 제어(0x03), 자율주차(0x04), 인증(0x05), 비상정지(0xFE)
    - 상태 서비스: AEB_STATE, AUTOPARK_STATE, TOF_DISTANCE, AUTH_STATE
- Control/Status 서비스별 요청–응답·이벤트 포맷 설계

**4) Qt6 기반 차량 제어 GUI 개발**
- 차량 제어 패널(8방향 주행, 속도, AEB, AutoPark, 인증 UI) 제작
- 실시간 상태 모니터링(ToF, AEB, Park 단계, Auth 결과)
- SOME/IP 메시지 로그 콘솔 개발
- Client RPi와의 연결 상태 모니터링 기능 구현

**5) 시스템 통합 및 팀장 역할**
- SOME/IP Client ↔ Server 구현체 통합
- CAN Gateway ↔ TC375 ECU 연동
- 전체 end-to-end 플로우 점검 및 기능 검증 리드
- 진단/OTA 팀과 코드 충돌 없이 상·하위 제어 구조 유지
- Confluence 문서화, Jira 일정 관리 진행

<br />**[성과 및 결과]**
- Ethernet(SOME/IP)–CAN Gateway 기반의 SOA 구조 완성  
    → 실차 구조와 동일한 SDV 아키텍처 구현 성공
- PC–RPi–TC375 간 End-to-End 제어 체인 구축    
    → GUI → SOME/IP → CAN → ECU 제어를 서비스 기반으로 성공적으로 연결    
- WSL 멀티캐스트 제약 해결    
    → 아키텍처 재설계(Client RPi 추가)로 SD 정상 동작    
- 팀장으로서 통합 및 품질 관리 수행    
    → 진단/OTA 모듈 포함한 전체 아키텍처 의사소통 및 일정 조율

#### **Tech Stack**
<img src="https://img.shields.io/badge/c-A8B9CC.svg?style=for-the-badge&logo=c&logoColor=white"> <img src="https://img.shields.io/badge/aurix-F37321.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/git-%23F05032.svg?style=for-the-badge&logo=git&logoColor=white"> <img src="https://img.shields.io/badge/github-%23181717.svg?style=for-the-badge&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/jira-%230052CC.svg?style=for-the-badge&logo=jira&logoColor=white"> <img src="https://img.shields.io/badge/confluence-%23172B4D.svg?style=for-the-badge&logo=confluence&logoColor=white"> <img src="https://img.shields.io/badge/autosar-E44D26.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/a--spice-C82333.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/iso--26262-D9534F.svg?style=for-the-badge&logoColor=white">

---

### Open-End Winding PMSM 영상전류 억제 기법 연구
**프로젝트 기간:** 2023년 3월 ~ 2023년 6월

두 개의 인버터에서 발생하는 공통 모드 전압(CMV)이 영상전류의 원인임을 파악하고, SVPWM에 옵셋 전압을 인가하는 제어 방식을 설계 및 검증하여 문제를 해결했습니다.

#### **My Role & Contributions**
- **회로 설계 및 시뮬레이션 주도:** 제어 방식 설계부터 시뮬레이션 검증까지의 전 과정을 주도했습니다.
- **성과:** 영상전류 피크값을 **2.65A에서 0.88A (약 67% 개선)** , 상전류 THD를 **26%에서 12% (약 54% 개선)** 로 낮추는 성능 개선을 이끌어냈습니다.

#### **Tech Stack**
<img src="https://img.shields.io/badge/matlab-%230076A8.svg?style=for-the-badge&logo=matlab&logoColor=white"> <img src="https://img.shields.io/badge/simulink-%230076A8.svg?style=for-the-badge&logo=matlab&logoColor=white">

---

### 학생복지위원회 시스템 개선 (총괄국장)
**활동 기간:** 2017년 3월 ~ 2019년 2월

학생복지위원회 총괄국장으로서 고질적인 대여 물품 관리 시스템의 문제를 해결하고, 조직 운영의 효율성과 투명성을 강화했습니다.

#### **My Role & Contributions**
- **대여 시스템 개선:** 수년간 방치된 재고 기록을 전수조사하고, '실시간 대여 관리 시스템'을 자체적으로 기획 및 구축하여 기존 대비 **물품 회수율을 3배 가까이 향상**시켰습니다.
- **이해관계자 갈등 중재:** 내부 구매팀(예산 중심)과 외부 협력사(납기·비용 중심) 간의 갈등 발생 시, 실사용 데이터를 분석하여 양측을 설득하고 협상을 주도하여 **물품 품질 향상과 신뢰 구축**을 동시에 이뤄냈습니다.

---

## 📝 Publications

### **동특성 향상을 위한 영구자석 동기전동기의 MMPC 기반 전류 제어 기법**
**발표 학회:** 2023년 하계 전력전자학술대회 (KIPE)

EV용 모터의 핵심 성능인 빠른 동특성 확보를 목표로, 새로운 구조의 MMPC 기법을 적용하여 기존 PI 제어기 대비 **과도상태 응답 시간을 64.7% 단축**시키는 성과를 거두었습니다. 연구 기획부터 수학적 모델링, 시뮬레이션 검증, 논문 작성 및 발표까지 모든 과정을 주도적으로 수행했습니다.

---

## 🛠️ Skills & Tech Stack

### 💻 Languages
<img src="https://img.shields.io/badge/c-A8B9CC.svg?style=for-the-badge&logo=c&logoColor=white"> <img src="https://img.shields.io/badge/c++-00599C.svg?style=for-the-badge&logo=cplusplus&logoColor=white"> <img src="https://img.shields.io/badge/python-3776AB.svg?style=for-the-badge&logo=python&logoColor=white">

### 🚗 Automotive & Embedded
<img src="https://img.shields.io/badge/RTOS-005A9B.svg?style=for-the-badge&logo=linux&logoColor=white"> <img src="https://img.shields.io/badge/FreeRTOS-E44D26.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/OSEK/VDX-C82333.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/CAN/CAN--FD-181717.svg?style=for-the-badge&logo=CAN-Bus&logoColor=white"> <img src="https://img.shields.io/badge/Ethernet-339933.svg?style=for-the-badge&logo=Ethernet&logoColor=white"> <img src="https://img.shields.io/badge/MQTT-660066.svg?style=for-the-badge&logo=MQTT&logoColor=white"> <img src="https://img.shields.io/badge/Secure%20OTA-D9534F.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/Power%20Electronics-F37321.svg?style=for-the-badge&logoColor=white">

### 🛠️ Tools
#### IDE & Editor
<img src="https://img.shields.io/badge/visual%20studio%20code-%23007ACC.svg?style=for-the-badge&logo=visualstudiocode&logoColor=white"> <img src="https://img.shields.io/badge/visual%20studio-%235C2D91.svg?style=for-the-badge&logo=visualstudio&logoColor=white"> <img src="https://img.shields.io/badge/Eclipse-2C2255.svg?style=for-the-badge&logo=Eclipse-IDE&logoColor=white">

#### Engineering & Simulation
<img src="https://img.shields.io/badge/matlab-%230076A8.svg?style=for-the-badge&logo=matlab&logoColor=white"> <img src="https://img.shields.io/badge/simulink-%230076A8.svg?style=for-the-badge&logo=matlab&logoColor=white"> <img src="https://img.shields.io/badge/CANoe-004E8A.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/Infineon%20AURIX-F37321.svg?style=for-the-badge&logo=infineon&logoColor=white"> <img src="https://img.shields.io/badge/UDE%20Visual%20Platform-005A9B.svg?style=for-the-badge&logoColor=white"> 

#### Development, Management & Test
<img src="https://img.shields.io/badge/gcc-%23A4261D.svg?style=for-the-badge&logo=gnu&logoColor=white"> <img src="https://img.shields.io/badge/git-%23F05032.svg?style=for-the-badge&logo=git&logoColor=white"> <img src="https://img.shields.io/badge/github-%23181717.svg?style=for-the-badge&logo=github&logoColor=white">
<img src="https://img.shields.io/badge/jira-%230052CC.svg?style=for-the-badge&logo=jira&logoColor=white"> <img src="https://img.shields.io/badge/confluence-%23172B4D.svg?style=for-the-badge&logo=confluence&logoColor=white"> <img src="https://img.shields.io/badge/Doxygen-2764A2.svg?style=for-the-badge&logo=Doxygen&logoColor=white">

### 📜 Standards
<img src="https://img.shields.io/badge/autosar-E44D26.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/a--spice-C82333.svg?style=for-the-badge&logoColor=white"> <img src="https://img.shields.io/badge/iso--26262-D9534F.svg?style=for-the-badge&logoColor=white">

<img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake.svg" alt="snake gif" />
