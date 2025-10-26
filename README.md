## PIC32-Study
PIC32 MCU 학습

### Tool
- MPLAB X IDE : 개발 전 과정(설계·코딩·빌드·디버그)
    - 사용자 : 펌웨어 개발자
    - 소스코드, 프로젝트 설정, 컴파일러(XC8/16/32 등)
    - 편집기, 빌드, 시뮬레이터, 디버거, 코드 생성기(MCC/Harmony)
- MPLAB X IPE : 생산/현장용 안전한 프로그래밍(Program/Verify)
    - 사용자 : 생산라인/테스터/현장 엔지니어/오퍼레이터
    - HEX/ELF 등 빌드 산출물
    - 프로그램/검증/읽기/지우기/공장모드 보안

### MCU
- PIC Core : PIC16F877A, PIC18F4520, PIC24FJ128GA010, dsPIC33EP512MU810
- MIPS : PIC32MX, PIC32MZ, PIC32MK
- ARM : PIC32CM, PIC32CX, PIC32CK

### 초기 설정
1. 클럭 설정

| 구분                          | 이름                              | 위치     | 기본 주파수               | 특징 / 용도                         |
| --------------------------- | ------------------------------- | ------ | -------------------- | ------------------------------- |
| **내부 오실레이터**                | **FRC (Fast RC Oscillator)**    | CPU 내부 | 8 MHz (조정 가능)        | 내부 발진기, 기본 부팅 및 테스트용, PLL 입력 가능 |
| **백업 내부 오실레이터**             | **BFRC (Backup FRC)**           | CPU 내부 | 8 MHz                | FRC 또는 POSC 오류 시 자동 전환용         |
| **저속 내부 오실레이터**             | **LPRC (Low Power RC)**         | CPU 내부 | 약 32 kHz             | 저전력 타이머, Watchdog용              |
| **외부 오실레이터**                | **POSC (Primary Oscillator)**   | 보드 외부  | 일반적으로 8 MHz / 24 MHz | 외부 크리스털 입력, 정밀도 높음              |
| **보조 외부 오실레이터**             | **SOSC (Secondary Oscillator)** | 외부     | 32.768 kHz           | RTC(Real-Time Clock)용           |
| **PLL (Phase Locked Loop)** | **SPLL / UPLL**                 | CPU 내부 | 200 ~ 400 MHz (가변)   | FRC 또는 POSC를 입력으로 받아 주파수 증폭     |

2. 디버깅 방법
3. WatchDog Timer
