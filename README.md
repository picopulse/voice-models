# voice-models

picoVoice(피코펄스 보이스) 온디바이스 STT용 모델 배포 저장소.

앱은 첫 실행 시 여기 릴리스에서 모델을 자동 다운로드합니다.

## 배포 모델

### `ggml-large-v3-turbo-ko-zeroth-q5_0.bin` (릴리스 `v1`)

한국어 음성인식 모델. Whisper large-v3-turbo 기반 한국어 파인튜닝(Zeroth-KO-v2)을
whisper.cpp ggml 포맷으로 변환 + q5_0 양자화한 것.

- 크기: 574,041,195 bytes (≈574MB)
- SHA256: `3ca01d7ca464b6be625e5abf291f555e2157d56d49a7797e41894a4ad5655010`
- 평가셋 CER 3.08% / 2.30%

## 출처 및 라이선스 (Attribution & Licenses)

이 모델은 아래 구성요소의 파생물이며, 각 출처를 고지합니다.

| 구성요소 | 저작자/출처 | 라이선스 |
|---|---|---|
| 베이스 모델 Whisper large-v3-turbo | OpenAI ([openai/whisper-large-v3-turbo](https://huggingface.co/openai/whisper-large-v3-turbo)) | MIT |
| 파인튜닝 체크포인트 | o0dimplz0o ([Whisper-Large-v3-turbo-STT-Zeroth-KO-v2](https://huggingface.co/o0dimplz0o/Whisper-Large-v3-turbo-STT-Zeroth-KO-v2)) | 미선언 (아래 주석 참고) |
| 학습 데이터셋 | o0dimplz0o ([Zeroth-STT-Korean](https://huggingface.co/datasets/o0dimplz0o/Zeroth-STT-Korean)) | Apache-2.0 |
| 원본 말뭉치 Zeroth-Korean | Goodatlas/Kaldi Zeroth project (Lucas Jo, Wonkyum Lee) | CC-BY-4.0 |
| 포맷 변환·양자화 도구 whisper.cpp | Georgi Gerganov | MIT |

> **파인튜닝 체크포인트 라이선스 주석**: 원저자가 모델카드에 라이선스를 명시하지
> 않았습니다. 본 재배포는 (a) 베이스 가중치가 MIT, (b) 학습 데이터가 Apache-2.0 /
> CC-BY-4.0로 상업적 이용·재배포가 허용된다는 점에 근거합니다. 원저자에게 명시적
> 라이선스 부여를 요청 중입니다.

CC-BY-4.0(Zeroth-Korean 말뭉치)에 따라 원 말뭉치 저작자에게 출처를 표기합니다.
