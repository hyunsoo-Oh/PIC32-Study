## PIC32MZ Curiosity 2.0

[Develop Board](https://www.digikey.kr/ko/products/detail/microchip-technology/DM320209/10444945?gclsrc=aw.ds&gad_source=1&gad_campaignid=21607947973&gbraid=0AAAAADrbLlgy-dOlFKmPvRTjZIH6crZ0K&gclid=CjwKCAjw6vHHBhBwEiwAq4zvA51OcipKDY-a7Zi1kwrM9efFfYBI2R-Iw4_oGpWHn4Izyoom94vS1RoCHDAQAvD_BwE)

[Curiosity 2.0 User Manual](https://ww1.microchip.com/downloads/en/DeviceDoc/Curiosity_PIC32MZEF2.0_Development_Board_Users_Guide_DS70005400A.pdf)

#### 목표
- I/O1 Xplained Pro Extension Kit에 있는 온도 센서의 현재 실내 온도 측정
    - 500ms(0.5초)마다 시리얼 콘솔(Serial Console)에 주기적으로 표시
- LED1은 온도 값이 시리얼 콘솔에 표시될 때마다 토글


### 주요 구성
| 항목            | 설명                                                                     |
| ------------- | ---------------------------------------------------------------------- |
| **MCU**       | PIC32MZ2048EFM 또는 PIC32MZ2064DA (MIPS32® M-Class Core, 최대 200~252 MHz) |
| **메모리**       | 최대 2 MB Flash, 512 KB SRAM, 16 KB Cache                                |
| **전원 입력**     | USB 5 V 또는 외부 12 V (온보드 LDO/DC-DC 변환 지원)                               |
| **디버깅/프로그래밍** | On-board **PICkit™ Onboard 3** (PKOB3) 내장 — 외부 디버거 불필요                 |
| **확장 슬롯**     | MikroBUS™ 2개, Arduino Uno 헤더, Pmod 인터페이스                               |
| **통신 인터페이스**  | USB HS OTG, Ethernet RMII, CAN, UART, SPI, I²C                         |
| **오디오/그래픽**   | CODEC IC (오디오 DAC/AMP), LCD 커넥터 (DA시리즈 전용)                             |
| **저전력 기능**    | Sleep/Idle 모드, 하드웨어 RTC, 외부 WAKE 핀                                     |
| **디버그 포트**    | USB-Serial Bridge (UART 통신 전용 Micro USB 포트)                            |

#### 교육용·확장용 모듈을 쉽게 꽂아 쓸 수 있는 표준 포트
MikroBus : Click Board를 2개까지 직접 꽂아 사용 가능

Prom : FPGA/Pmod 모듈 바로 연결 가능

```Arduino
 ┌─────────────────────────────┐
 │       PIC32MZ MCU           │
 │  ─────────────────────────  │
 │  CPU (MIPS32) @200MHz       │
 │  2MB Flash / 512KB SRAM     │
 │  FPU, DSP Engine 포함        │
 │  ─────────────────────────  │
 │  USB OTG, CAN, UART, SPI    │
 │  I2C, ADC, PWM, Timers      │
 └────────────┬────────────────┘
              │
 ┌────────────┼────────────┐
 │            │            │
 ▼            ▼            ▼
 MikroBUS    Arduino      Ethernet
  Socket     Header       RMII PHY

```

