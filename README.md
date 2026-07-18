# voice-models

picoVoice(피코펄스 보이스) 온디바이스 STT용 모델 배포 저장소.

앱은 첫 실행 시 여기 릴리스에서 모델을 자동 다운로드합니다.

## 배포 모델

### picoV-KO — `ggml-large-v3-turbo-ko-picoV-q5_0.bin` (릴리스 `v2`)

picopulse가 자체 학습한 한국어 음성인식 모델. Whisper large-v3-turbo 기반 파인튜닝을
whisper.cpp ggml 포맷으로 변환 + q5_0 양자화한 것.

- 크기: 574,041,195 bytes (≈574MB)
- SHA256: `da6c9fe5e18f0752cff5828fb24375f50467a371aab9b4985a7a0c491c7c676d`

> 같은 릴리스의 `ggml-large-v3-turbo-ko-kspon-q5_0.bin`은 동일 모델의 구 파일명으로,
> 구버전 앱(≤0.8.4) 호환을 위해 한시 유지됩니다.

## 라이선스 (License)

**picoV-KO 모델 가중치는 picopulse의 저작물입니다.**
picoVoice 앱의 정상적인 사용(앱이 수행하는 자동 다운로드) 목적 외의
**재배포, 타 제품·서비스 탑재, 상업적 이용을 금지합니다.**
그 외 이용은 picopulse(picopulsekorea@gmail.com)와 별도 협의가 필요합니다.

The picoV-KO model weights are proprietary to picopulse. Redistribution, use in
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

- `v2` — 현행 STT 모델 (picoV-KO)
- `app-vX.Y.Z` — picoVoice 앱 설치본
- `updater` — 앱 자동 업데이트 매니페스트 (latest.json)
