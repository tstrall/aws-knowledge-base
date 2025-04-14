# LLMs (Large Language Models)

**What they are:**
- Large Language Models (LLMs) are deep learning models trained on massive text corpora to understand and generate human-like language
- Examples: GPT, Claude, PaLM, LLaMA, Mistral, Gemini

---

## Key Concepts

| Concept              | Description |
|----------------------|-------------|
| **Transformer**      | Neural architecture enabling attention-based learning (Vaswani et al., 2017) |
| **Token**            | Basic unit of input (word pieces, subwords) |
| **Context Window**   | Maximum token length the model can attend to in one prompt |
| **Fine-tuning**      | Training on task-specific data to specialize the model |
| **Embedding**        | Vector representation of words or sentences |
| **Prompt Engineering** | Designing input text to control model behavior |

---

## Training Pipeline
1. **Pretraining**: Predict next token from large-scale general text (self-supervised)
2. **Alignment**: Use reinforcement learning (e.g., RLHF) to align output with human intent
3. **Fine-tuning**: Adapt model to specific domains or tasks

---

## Inference Use Cases
- **Chatbots & Assistants**
- **Code generation** (e.g., Copilot, CodeWhisperer)
- **Search/QA** (retrieval-augmented generation)
- **Summarization, translation, rewriting**
- **Agentic workflows** (tool use, planning, multi-step logic)

---

## Models to Know
| Model     | Notes |
|-----------|-------|
| **GPT-4** | OpenAI's most capable model (as of 2024) |
| **Claude** | Anthropic's assistant with long context support |
| **Gemini** | Google's family (formerly Bard/PaLM) |
| **LLaMA** | Meta’s open model suite (LLaMA 2, Code LLaMA, LLaMA 3) |
| **Mistral** | Lightweight, fast open model for on-prem or edge use |

---

## Limitations
- Can hallucinate (make confident errors)
- Sensitive to prompt phrasing and token limit
- Prone to misuse if not filtered or constrained
- Interpretability remains an open challenge

---

## Tools & Ecosystem
- **LangChain** / **LlamaIndex**: LLM orchestration frameworks
- **OpenAI API / Hugging Face**: Model access and hosting
- **Vector DBs**: Pinecone, Weaviate, FAISS (used for semantic search)
- **Prompt injection defense**: Guardrails, input sanitization, output filters

---

## Interview Tips
- Understand the basic architecture and limitations of LLMs
- Be able to describe how transformers and attention work at a high level
- Know real-world use cases where LLMs help or fail
- Mention prompt engineering, grounding via RAG, and when fine-tuning is justified
