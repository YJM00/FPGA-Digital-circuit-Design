# FPGA-Digital-circuit-Design

# 🖥️ System-on-Chip Design & Practice (ZYNQ + FPGA + ARM 실습)

**Xilinx Vivado & Vitis 툴**을 활용하여  
FPGA(PL)와 ARM Cortex-A53(PS)이 결합된 **ZYNQ SoC** 환경에서  
디지털 회로를 설계하고, 다양한 주변 장치를 제어하는 실습을 진행하였다.

---

## ⚙️ 개발 환경
- **툴**:
  
![sadsad12](https://github.com/user-attachments/assets/58905e78-a2cb-4c54-bb6e-4120e78546ac)


<img width="450" height="300" alt="1wx" src="https://github.com/user-attachments/assets/af50dc58-e290-4b30-a396-1a9455fcb748" />

- **언어**: Verilog HDL, C
- **보드**: ZYNQ 기반 실습 키트
- <img width="542" height="526" alt="image" src="https://github.com/user-attachments/assets/9b146a50-26dd-4c8e-8148-70b047324f68" />

  (Text LCD, 7-Segment, LED, TFT-LCD, Camera, Step Motor, Ultrasonic Sensor, etc.)

---

## 📌 주요 학습 내용

### 1. Vivado를 통한 FPGA 회로 설계
- Verilog HDL을 이용한 디지털 회로 설계
- **Constraints 파일(XDC)** 을 통한 핀 매핑
- 합성(Synthesis) → 구현(Implementation) → 비트스트림(Bitstream) 생성

### 2. Block Design & AXI Interface
- Vivado Block Design을 이용해 **ZYNQ PS + Custom IP(PL)** 연결
- AXI4-Lite 인터페이스를 활용해 **PS(ARM)과 PL(FPGA) 간 데이터 교환**
- XSA 파일을 생성하여 Vitis로 연동

### 3. Vitis를 통한 PS 영역 코딩
- ARM Cortex-A53 기반 **C 코드 작성 및 실행**
- FPGA에 구현된 7-Segment IP와 AXI 인터페이스로 통신
- `xil_io.h` 라이브러리를 이용한 레지스터 접근 및 값 출력

---

## 🔬 실습한 주변 장치 제어

- **7-Segment**
  - FPGA Verilog로 디코더 설계
  - AXI 인터페이스를 통해 ARM에서 값 전달
  - FPGA와 ARM 협업으로 시간 표시/카운터 구현

- **Text LCD**
  - FPGA → AXI IP 생성
  - ARM에서 문자열 출력 및 갱신

- **LED / Slide Switch / Push Button**
  - 단순 I/O 제어 및 인터럽트 처리 실습

- **Step Motor / Ultrasonic Sensor**
  - AXI GPIO 및 PWM 제어
  - 거리 측정 및 모터 회전 구현

- **TFT-LCD & CSI-Camera**
  - 이미지 데이터 송수신
  - PS에서 처리 후 디스플레이 출력 테스트

---

## 📈 배운 점
- HDL 설계와 SoC 통합 흐름 이해 (Vivado → Bitstream → Vitis)
- FPGA(PL) + ARM(PS) 간 협업 구조 경험
- 데이터시트 기반 핀 매핑과 제약 조건 작성 능력 향상
- 단순 시뮬레이션을 넘어 실제 하드웨어 제어 및 디버깅 능력 강화

---

## 📝 후기
이번 수업을 통해 **ZYNQ SoC 설계 전 과정**을 실습할 수 있었고,  
단순 논리 회로 설계가 아닌 **ARM과 FPGA의 융합 개발 경험**을 얻을 수 있었다.  
7-Segment뿐 아니라 다양한 모듈을 직접 테스트하면서,  
**하드웨어-소프트웨어 코디자인( HW/SW Co-Design )**의 개념을 실질적으로 이해하게 되었다.
