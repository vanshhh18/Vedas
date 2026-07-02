# Vedaz AI Assessment – Qwen Fine-tuning

## Overview

This repository contains my submission for the Vedaz AI technical assessment.

The objective was to:

- Fine-tune a Qwen2.5 model on the provided astrology chat dataset.
- Document the process of hosting the model on a VPS using vLLM.
- Create five manually written astrology conversations suitable for instruction tuning.

---

## Model

- **Base Model:** Qwen2.5-3B-Instruct
- **Fine-tuning Method:** LoRA (QLoRA)
- **Frameworks:** Hugging Face Transformers, TRL, PEFT
- **Language:** Hindi & English
- **Task:** AI Vedic Astrologer Chat Assistant

---

## Dataset

The model was fine-tuned on the assessment dataset provided by Vedaz.

The dataset is **not included** in this repository because it was provided solely for the assessment.

---

## Training Configuration

| Parameter | Value |
|----------|-------|
| Model | Qwen2.5-3B-Instruct |
| Fine-tuning | LoRA |
| Epochs | 8 |
| Learning Rate | 1e-4 |
| Batch Size | 1 |
| Gradient Accumulation | 8 |
| Optimizer | AdamW |
| Framework | TRL SFTTrainer |

---

## Project Structure

```
.
├── finetune_qwen.ipynb
├── Hosting_with_vLLM.pdf
├── Five_Training_Chats.pdf
└── README.md
```

---

## Fine-tuning Workflow

1. Loaded and inspected the provided chat dataset.
2. Converted conversations into the Qwen chat template.
3. Fine-tuned the model using LoRA with TRL's `SFTTrainer`.
4. Evaluated the model through manual inference on unseen prompts.
5. Saved the trained adapter for inference.

---

## vLLM Deployment

The repository includes a deployment guide covering:

- VPS requirements
- Installing vLLM
- Launching the OpenAI-compatible API server
- Testing inference endpoints
- Production deployment considerations

See:

**Hosting_with_vLLM.pdf**

---

## Manual Training Conversations

Five manually written conversations were created following the required style:

- Empathetic responses
- Kundli analysis
- Asking the user to wait while the chart is analyzed
- Balanced astrology guidance
- Safe and non-fatalistic predictions

See:

**Five_Training_Chats.pdf**

---

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- TRL
- PEFT
- BitsAndBytes
- vLLM

---

## Notes

This project was completed as part of the Vedaz AI technical assessment.

The dataset used for training is not redistributed in this repository.
