---
title: Inside Home
keywords: sample
summary: "유니티를 이용한 게임 제작"
sidebar: product2_sidebar
permalink: p2_sample3.html
simple_map: true
map_name: usermap
box_number: 3
folder: product2
---
# Inside Home – 유니티를 이용한 게임 제작

<iframe width="560" height="315" src="https://www.youtube.com/embed/3OM7SGs73jA?si=53yVkAyMkfmHxAr9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>  

## 🎮 프로젝트 개요
Unity와 OpenXR 기반으로 제작된 AR/VR 전환형 퍼즐 게임입니다.  
게임 초반에는 AR 환경에서 시작하여 오브젝트와 상호작용하다가, 특정 조건에서 VR 공간으로 진입하여 방마다 주어진 퍼즐을 해결하며 진행하게 됩니다.

---

## 🛠 기술 스택
- **Unity** 6000.0.57f1 (6.0)
- **OpenXR**
- **Android Build 지원**
- **Meta All-in-one SDK** (Quest3 포함)

---

## 📖 게임 초반 흐름
1. **AR 화면 시작**  
   - 스피커와 집 모양의 에셋이 배치됩니다.
   - 스피커를 눌러 소리를 조절하며 XR 상호작용을 경험합니다.
   - 집 모양 에셋을 집어 회전해본 뒤, 내려놓거나 던지면 **VR 공간으로 전환**됩니다.

2. **VR 진입 후**  
   - 세 개의 방(창고, 거실, 주방)에 순차적으로 입장합니다.
   - 각 방 입구에는 투명벽이 있으며, 문제를 해결해야 통과할 수 있습니다.
   - 문제 해결 시 배경 음악이 바뀌고, 투명벽이 해제됩니다.
   - 주요 힌트는 **손전등 빛**으로 숨겨진 글자를 밝혀내는 방식으로 제공합니다.

---

## 🗂 프로젝트 생성 방법
1. Git에서 받은 폴더 중 **Assets**, **ProjectSettings**, **Packages** 폴더를 임의의 이름이 붙은 빈 폴더 하위로 이동.
2. Unity Hub → Projects → **Add** → 해당 폴더 선택.  
   → Unity가 ProjectSettings와 Packages 설정을 인식하여 동일한 버전 환경으로 프로젝트가 열립니다.

---

## 💻 실행 방법
- **PC 테스트**  
  1. Hierarchy에서 `XR Device Simulator` 활성화.  
  2. 상단 Play ▶ 버튼 클릭.  
  3. 일시정지 버튼을 끄면 실제 상호작용 테스트 가능.

- **Meta Quest3 (VR 기기) 빌드**  
  1. `File → Build Profiles`에서 Android 플랫폼 선택 후 **Switch Platform**.  
  2. Run Device에 Quest 기기가 잡히는지 확인.  
  3. Build 또는 Build & Run 실행.

---

## 🏠 방 구성 및 퍼즐 설명

### 1️⃣ 창고 (첫 번째 방)
- 어두운 방 안에서 유일하게 **손전등**을 발견.
- 손전등을 비춰 **전기 배전함**을 탐색합니다.

#### ⚡ 전기 배전함 퍼즐 흐름
1. **퓨즈 삽입 단계**  
   - `FuseSlotTracker` 2개가 모두 꽂혀야 `FuseGateManager`가 메인 스위치 조작을 허용.
2. **메인 스위치 (검정 스위치, -90° 회전)**  
   - `MainSwitchSimpleDriverSmoothed`로 -90° 위치일 때만 `MainSwitchState`가 ON 처리.  
   - 이 스위치가 활성화되면 붉은 KnifeSwitch가 동작 가능.
3. **붉은 KnifeSwitch 조작**  
   - `KnifeSwitchSnap`을 통해 ON/OFF 제어.  
   - **ON:** 램프 점등 + 투명벽 해제.  
   - **OFF:** 램프 소등 + 투명벽 다시 활성화.  
   - OFF 전환 시 스프링으로 자동 복귀.

#### 🏆 결과
- 모든 단계를 성공적으로 수행하면 방에 불이 켜지고, 다음 스테이지로 갈 수 있는 투명벽이 해제됩니다.

---

### 2️⃣ 거실 (두 번째 방)
- 커다란 시계에서 시침과 분침이 사라진 상태로 째깍거림.
- 옷장을 열어도 아무것도 없으나, 연결된 방의 TV 쪽 구조를 보면 **대칭 구조**임을 확인.
- 차이가 나는 물체(촛대)를 찾아 가져옴.
- 다시 시계로 돌아와 손전등으로 벽/바닥에서 힌트를 발견.  
  그 힌트를 기반으로 시계 바늘을 맞추면 투명벽 해제.

---

### 3️⃣ 주방 (세 번째 방, 최종 공간)
- 켜진 오븐은 동작하지 않음.
- 냉장고를 조작하면 오븐 완료음과 함께 라이트가 꺼짐.
- 오븐에서 **출입증**을 획득.  
- 냉장고 옆 **태그기**에 출입증을 태그하면 냉장고가 열림.  
- 특정 추가 행동으로 최종 **탈출문** 생성.

---

## 🔦 손전등 시스템
- **HandLight.prefab**: XR Grab 가능 손전등 프리팹.  
- **FlashlightToggleByHeldHand**: 잡은 손의 버튼(A/B 또는 X/Y)으로 라이트 On/Off 제어.  
- **SpotRevealBinder**: 라이트 콘 내부에서만 특정 텍스트/오브젝트 표시(머티리얼 기반).  
- **FlashlightBeamTrigger + Revealable**: 빔 트리거 충돌 시 글자 On/Off (콜라이더 기반).  
- **RevealBySpot.shader**: 라이트 콘 안에서만 보이는 셰이더.  

---

## 🎨 UI/UX 기능

### 🔊 Speaker – 배경음 조절
- **SoundSetting Variant.prefab**을 통해 스피커 오브젝트와 상호작용하면 **게임 배경음 볼륨**을 조절할 수 있습니다.  
- 게임 초반 AR 공간에서 XR 상호작용 체험 요소로 배치되었습니다.

### 🚪 Exit Door – 게임 종료 및 탈출구
- **GameExit Canvas Variant.prefab** + `GameExit.cs`  
  - 초기 화면(Canvas)에서 Exit 버튼을 누르면 `QuitGame()` 실행 → **에디터에서는 Play 모드 종료 / 빌드에서는 Application.Quit()**.  
- **ExitDoor.png, Exitdoor2.png**  
  - 주방 퍼즐 최종 단계에서 탈출구로 활용.  
  - 최종 기믹 성공 시 Exit Door가 활성화되어 엔딩 연출.

---
