# Task.Text-generation

# Dialog Summarization with LoRA Fine-tuning

## 📌 Описание проекта

Дообучение модели **Qwen/Qwen2.5-1.5B-Instruct** на датасете **DialogSum** для задачи суммаризации диалогов с использованием **LoRA** (Low-Rank Adaptation).

---

## 📊 Результаты

### Сравнение метрик ROUGE/BLEU

| Метрика | Baseline | Zero-shot | Fine-tune |
|:--------|---------:|----------:|----------:|
| **ROUGE-1** | 0.1672 | 0.2261 | **0.2123** |
| **ROUGE-2** | 0.0517 | 0.0485 | **0.0888** |
| **ROUGE-L** | 0.1458 | 0.1678 | **0.1571** |
| **BLEU** | – | 0.0267 | **0.0275** |

### LLM-as-Judge (Groq, Llama 3.3 70B)

| Критерий | Средний балл (1-5) |
|:---------|:---:|
| **Relevance** | 3.8 |
| **Conciseness** | 4.4 |
| **Fluency** | 5.0 |
| **Общий** | **4.4** |

---

## 🖥️ Установка

```bash
pip install -q transformers peft accelerate bitsandbytes datasets
pip install -q rouge-score nltk
pip install -q groq
