# voice-models

피코보이스(picoVoice) 온디바이스 음성인식(STT) 모델과 앱 업데이트 배포 저장소.

앱은 첫 실행 시 여기 릴리스에서 모델을 자동 다운로드합니다.

## 배포 모델

### picoV2 — `ggml-large-v3-turbo-ko-picoV2-q5_0.bin` (릴리스 `v2`)

피코펄스가 자체 학습한 한국어 음성인식 모델. Whisper large-v3-turbo 기반 파인튜닝을
whisper.cpp ggml 포맷으로 변환 + q5_0 양자화한 것.

- 크기: 574,041,195 bytes (≈574MB)
- SHA256: `b0dfd719e6c0e89c00e0eca9eb36fbcf2cbfa549efddf2bcb7194a046b8ab77b`

> 같은 릴리스의 `ggml-large-v3-turbo-ko-picoV-q5_0.bin`과 `ggml-large-v3-turbo-ko-kspon-q5_0.bin`은
> 이전 모델(같은 가중치, 두 파일 이름)로, 구버전 앱(≤0.8.4) 호환을 위해 한시 유지됩니다.

## 라이선스 (License)

**이 저장소에서 배포하는 모델 가중치는 피코펄스(PICOPULSE)의 저작물입니다.**
피코보이스 앱의 정상적인 사용(앱이 수행하는 자동 다운로드) 목적 외의
**재배포, 타 제품·서비스 탑재, 상업적 이용을 금지합니다.**
그 외 이용은 피코펄스(info@picopulse.kr)와 별도 협의가 필요합니다.

The model weights distributed here are proprietary to PICOPULSE. Redistribution, use in
other products or services, and commercial use outside the picoVoice app are
prohibited without prior written permission.

## 출처 고지 (Attribution)

| 구성요소 | 저작자/출처 | 라이선스 |
|---|---|---|
| 베이스 모델 Whisper large-v3-turbo | OpenAI ([openai/whisper-large-v3-turbo](https://huggingface.co/openai/whisper-large-v3-turbo)) | MIT |
| 포맷 변환·양자화 도구 whisper.cpp | The ggml authors | MIT |

본 모델은 과학기술정보통신부와 한국지능정보사회진흥원(NIA)의
AI허브([aihub.or.kr](https://www.aihub.or.kr)) 데이터를 활용하여 개발되었습니다.

## 릴리스 구조

- `v2` — 현행 음성인식 모델 (picoV2)
- `app-vX.Y.Z` — 피코보이스 앱 설치본
- `updater` — 앱 자동 업데이트 매니페스트 (latest.json)
- `llama-b11393-signed` — 요약 실행 엔진 llama.cpp b11393 (Windows Vulkan x64) 원본
