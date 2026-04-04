# Mistral-7B Retail Banking Chatbot (QLoRA Fine-Tuning)

## Overview
This project focuses on adapting a general-purpose LLM (Mistral-7B) to a domain-specific task — retail banking customer support. The model is fine-tuned to generate structured and relevant responses to banking queries.

## Problem
Pretrained LLMs often produce generic responses that lack domain-specific accuracy. This project improves response quality by fine-tuning on a curated banking dataset.

## Approach
- Model: Mistral-7B-v0.3  
- Fine-tuning: QLoRA (PEFT)  
- Quantization: 4-bit (BitsAndBytes)  
- Dataset: Bitext Retail Banking (1000 samples)  
- Training: 1 epoch, batch size 1, gradient accumulation  

## Results
| Metric | Score |
|--------|------|
| ROUGE-1 | 0.4737 |
| ROUGE-L | 0.3452 |
| BLEU | 0.1182 |
| Task Accuracy | 80% |

## Example Output

**User Query:**  
I haven't received my refund yet, what should I do?

**Model Response:**  
- Check your bank or credit card statement  
- Contact customer support if refund is not processed  
- Follow official banking support channels  

## Key Learnings
- Efficient fine-tuning of large models using QLoRA  
- Working with domain-specific conversational datasets  
- Evaluating LLM outputs using multiple metrics  

## Limitations
- Small dataset (1000 samples)  
- Single epoch training  
- Limited generalization for edge cases   

## Tech Stack
- Python  
- Hugging Face Transformers  
- PEFT (QLoRA)  
- BitsAndBytes  
- Evaluate  
