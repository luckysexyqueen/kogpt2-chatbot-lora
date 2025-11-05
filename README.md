---
license: cc-by-nc-nd-4.0
base_model: skt/kogpt2-base-v2
tags:
- gpt2
- lora
- korean
- chatbot
language:
- ko
---
# 모델 이름
LoRA_텍스트_생성_HF_모델
## 모델 설명
base_model: skt/kogpt2-base-v2
## 모델 상세
언어 : 한국어
## LoRA 설정

## 학습 설정

## 학습 결과

## 사용 방법

```
# 1. 토크나이저 불러오기
tokenizer_reload = AutoTokenizer.from_pretrained(model_name_upload)

# 2. 베이스 모델 불러오기
base_reload = AutoModelForCausalLM.from_pretrained("skt/kogpt2-base-v2")

# 3. 학습할 때와 똑같이 크기 조정
base_reload.resize_token_embeddings(len(tokenizer_reload))
base_reload.config.pad_token_id = tokenizer_reload.pad_token_id

# 4. LoRA 불러오기
model_reload = PeftModel.from_pretrained(base_reload, model_name_upload)

```

## 모델 정보

