# LoRA 기반 Stable Diffusion 자동차 이미지 파인튜닝 모델
🚗🚗🚗  <br>
이 저장소는 sd-legacy/stable-diffusion-v1-5 모델을 베이스로, <br>
자동차 이미지에 특화된 LoRA(Low-Rank Adaptation) 파인튜닝을 수행한 프로젝트입니다.  <br>
LoRA를 이용해 경량화된 어댑터 레이어만 학습하여, 원본 모델 가중치는 그대로 유지하면서 자동차 이미지를 생성하는 품질을 향상시킵니다.

<br>

## 주요 단계
1. **샘플링 이미지 수집**  
   - AI 학습용 자동차 이미지 데이터셋 수집  
2. **데이터셋 전처리**  
   - 이미지 리사이징, 정규화  
   - 텍스트 프롬프트 매칭  
3. **LoRA 데이터셋 구성**  
   - `datasets/` 폴더에 학습/검증용 JSON 혹은 CSV 포맷 생성  
4. **LoRA 트레이닝**  
   - 경량화된 LoRA 어댑터 레이어만 학습  
   - 결과물: `.safetensors` 포맷의 LoRA 가중치 파일  
5. **모델 로딩 및 추론**  
   - Stable Diffusion v1.5 + 학습된 LoRA 어댑터 병합  
   - 고품질 자동차 이미지 생성

<br>

## repo 구조
리포지토리의 주요 파일 및 디렉토리는 다음과 같습니다:
README.md: 프로젝트 개요 및 설명을 담고 있는 문서입니다.
Loras/: 훈련된 LoRA 모델 파일이 저장되는 디렉토리입니다.
Lora_Trainer.ipynb: LoRA 모델을 훈련시키는 Jupyter Notebook 파일입니다.
Lora_dataset.ipynb: 모델 훈련에 사용할 데이터셋을 준비하는 Jupyter Notebook 파일입니다.

<br>

## LoRA 기반 모델 훈련 절차
샘플링 이미지 수집: 자동차 이미지를 수집하여 모델 학습에 필요한 데이터를 준비합니다.
데이터셋 제작: 수집한 이미지를 기반으로 LoRA 모델 훈련에 적합한 데이터셋을 생성합니다.
LoRA 모델 훈련: 준비된 데이터셋을 사용하여 LoRA 모델을 훈련시킵니다.
<img width="1310" height="716" alt="image" src="https://github.com/user-attachments/assets/3bd5f7d8-b2c2-47ef-ac41-0680abcd7114" />


<br>

## 요약
이 프로젝트는 Stable Diffusion v1.5 모델을 자동차 이미지 생성에 특화된 LoRA 모델로 파인튜닝하는 과정을 다루고 있습니다.  
효율적인 학습을 위해 LoRA 기법을 적용하였으며, 관련된 데이터셋 준비와 모델 훈련 과정을 Jupyter Notebook 파일을 통해 제공합니다.  

<br>

## 참고 자료
🤗 Hugging Face – Diffusers: https://github.com/huggingface/diffusers  
LoRA 논문: https://arxiv.org/abs/2106.09685  
Stable Diffusion v1.5: https://huggingface.co/runwayml/stable-diffusion-v1-5  

<br>

