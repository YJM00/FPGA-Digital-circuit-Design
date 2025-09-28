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

## 📈 이해한 점
- **FPGA와 ARM의 협력 구조**: PL은 병렬 연산/하드웨어 가속, PS는 제어 및 소프트웨어 로직 담당  
- **AXI 인터페이스 동작 원리**: 레지스터 기반 데이터 전송 방식 및 IP 통합 흐름  
- **하드웨어-소프트웨어 통합 개발**: HDL 설계, 핀 제약, 비트스트림, 드라이버, C 코드까지의 전체 개발 사이클  
- **디버깅 중요성**: 시뮬레이션과 실제 보드 동작 차이를 직접 확인하며 하드웨어 디버깅 경험 축적  

---

## 🚀 할 수 있게 된 것
- Verilog로 **디지털 회로 모듈 설계 및 테스트** 가능
- Vivado를 이용해 **Constraints 작성 → 합성 → 비트스트림 생성** 가능
- **Custom AXI IP 설계** 및 ZYNQ PS와의 연동 가능
- Vitis에서 ARM 기반 **C 코드 작성 → 하드웨어 제어** 가능
- 다양한 보드 모듈(7-Segment, LCD, 모터 등) 제어 및 테스트 경험 보유
- **SoC 기반 임베디드 시스템 프로젝트 설계** 경험 응용 가능

---

## 📝 후기
이번 수업을 통해 단순 논리 회로 설계를 넘어서 **ZYNQ SoC 통합 개발 프로세스**를 경험했다.  
특히 **하드웨어-소프트웨어 코디자인(HW/SW Co-Design)** 과정을 직접 실습하며  
FPGA와 ARM의 협력 구조, AXI 인터페이스의 실제 동작 방식을 이해할 수 있었다.  
이제는 새로운 하드웨어 모듈이 주어져도, Vivado에서 IP를 설계하고 AXI로 연결한 뒤,  
ARM 코드에서 직접 제어할 수 있는 자신감을 가지게 되었
