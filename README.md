## [파비콘이미지] Giggle Forest (project.VoiceSpace) by Team - under5

### 개발 목적

코로나 시대를 겪으면서 대부분의 '만남의 장소'가 각종 Zoom에서 파생된 각종 화상회의 공간으로 빠르게 이동 하고 있습니다. 그런 만큼 부작용도 많은데 대표적으로 화상회의 에서 평소의 대화보다 훨씬 많은 피로도를 느끼는 [줌피로도 (Zoom Fatigue)](https://en.wikipedia.org/wiki/Zoom_fatigue)증상이 대두 되고 있습니다. 이러한 피로의 주요 원인을 저희는

1. 영상
2. 딱딱한 화상회의 공간

라고 분석하였고, 이에 따라 **영상없는, 현실감 있는 대화**,**부드럽고 즐거운 공간**을 제공하는 서비스를 만들려는 목적으로 개발을 시작하였습니다.

---

### 소개 동영상
[![YoutubeVideo](https://img.youtube.com/vi/ZcalOaRKCv8/maxresdefault.jpg)](https://www.youtube.com/embed/ZcalOaRKCv8)

---

### 개발 및 배포 환경

| Part                       | Environment | Remark(Version) |
| -------------------------- | ----------- | --------------- |
| Front                      | React       | 17.0.2          |
| Back                       | NestJS      | 7.6.15          |
| WebServer                  | Nginx       | 1.14.2          |
| Publishing Server Hardware | AWS         | EC2             |

---

### 주 사용 라이브러리

| Name        | Remark                                                                        |
| ----------- | ----------------------------------------------------------------------------- |
| WebRTC      | 유저간 끊김없는 음성, 데이터 전송                                             |
| WebGL       | 영상을 대신하는 애니메이션을 클라이언트의 그레픽처리 하드웨어를 사용하여 출력 |
| WebAudioAPI | 영상없이도 현실감있는 대화를 구현하기 위한 음성분석 및 컨트롤                 |
| Jest        | 구현된 Component들과 Class의 Unit, Integration Test                           |

---

### 시스템 구성도
#### 전체적인 시스템 구성
![image](https://user-images.githubusercontent.com/74593890/131950983-cf735bf4-3a74-4074-bf3d-1bf79e3fc6cd.png)
#### 다수의 Peer 연결 방식
![Advantages and disadvantages of mesh topology - IT Release](https://www.itrelease.com/wp-content/uploads/2021/06/Full-Mesh-Topology-1024x640.jpg)

---
### 주요 기능
- WebGL 을 이용한 굉장히 부드러운 애니메이션 (눈의 피로감 감소)
- WebRTC 를 이용한 현실과 같은 매우 낮은 레이턴시의 음성채팅 (딜레이로부터 오는 피로감 감소)
- Avatar 끼리의 거리가 멀어질수록, 음성 볼륨도 낮아지는 기능 (현실감 있는 음성 채팅)
- 목소리 크기에 따라 아바타의 얼굴 크기가 변함 (현실감 있는 음성 시각화)
![gif](https://user-images.githubusercontent.com/74593890/131952354-8176e60f-da09-4b66-9d6a-1356eb40a7d6.gif)

---

### 주요 추가중인 기능 (고도화)
- 음성을 분석하여 해당 발음에 맞게 아바타의 입모양이 바뀌는 기능 (현실감 있는 음성 채팅)
- 아바타들이 움직이는 맵을 커스터마이징 하는 기능

---

### 프로젝트 시작하기

in back folder

```
npm install
npm run start:dev
```

in front folder

```
npm install
npm run start
```
- front 폴더의 .env.development 에서 백엔드 주소를 변경 하실 수 있습니다.

---

### 문서
- 각종 Component, Class, Function 정보는 [여기](https://voicespaceunder5.github.io/VoiceSpaceDocs) 서 확인 하실 수 있습니다.

---

### 팀원

| Name     | Email               | Role | Major Part                    | Minor Part | Tech Stack                                   |
| -------- | ------------------- | ---- | ----------------------------- | ---------- | -------------------------------------------- |
| kilee    | (이메일 주소)       | 팀장 | 디자인, 프로젝트 배포 및 관리 | Front      | AWS, Github Action, CI/CD, React, Typescript |
| honlee   | kij753@naver.com    | 팀원 | Front                         | Back       | AWS, React, NestJS, Typescript               |
| hyeonkim | hyongtiii@gmail.com | 팀원 | Back                          | Front      | React, NestJS, Typescript                    |
| mijeong  | minje70@naver.com   | 팀원 | Front                         | Back       | React, NestJS, Typescript                    |

---
