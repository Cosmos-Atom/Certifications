# Section 1: Fundamentals of Generative AI
**~30% of the exam**

---

## Core Hierarchy: AI → ML → Deep Learning → Gen AI

| Term | Definition |
|------|-----------|
| **Artificial Intelligence (AI)** | Building machines that perform tasks requiring human intelligence: learning, problem-solving, decision-making |
| **Machine Learning (ML)** | A subfield of AI where machines learn from data to perform specific tasks |
| **Deep Learning** | A subset of ML that uses artificial neural networks with many layers to extract complex patterns |
| **Generative AI** | An application of ML that focuses on **creating new content** |

> Visual: Gen AI ⊂ Deep Learning ⊂ ML ⊂ AI

---

## What is Generative AI?

Gen AI creates new content and ideas. Applications can be **multimodal** — processing and generating text, images, code, and audio simultaneously.

Gen AI can:
- **Create** — Generate new content
- **Summarize** — Condense information into concise summaries
- **Discover** — Find information at the right time
- **Automate** — Automate previously manual tasks

---

## Foundation Models and LLMs

### Foundation Models
- Large AI models trained on **massive amounts of unlabeled data**
- Allow broad understanding of the world
- Three key features:
  - **Trained** on diverse data
  - **Flexible** to a wide range of use cases
  - **Adaptable** to specialized domains through additional, targeted training

### Large Language Models (LLMs)
- A type of foundation model designed to **understand and generate human language**
- Trained on **vast datasets** — this is their core strength
- Enable broad language and context understanding, adaptability across many tasks
- NOT: limited to niche tasks, effective with small datasets, inherently strong reasoners without prompting

**Key insight from sample exam:** LLMs are known for being trained on vast datasets enabling broad context understanding — not for deep singular domain expertise.

---

## Data Types

### By Labeling
| Type | Description |
|------|-------------|
| **Labeled data** | Data with associated tags (name, type, number) — used for supervised learning |
| **Unlabeled data** | Raw, unprocessed information without tags (e.g., audio streams, unorganized photos) |

### By Structure
| Type | Description |
|------|-------------|
| **Structured data** | Organized, easy to search — stored in relational databases |
| **Unstructured data** | Lacks predefined structure — requires sophisticated analysis |
| **Quality data** | Accurate, complete, consistent, and relevant |
| **Accessible data** | Readily available, usable, and in the proper format for model training |

**Key insight from sample exam:** Emails tagged with categories like "Billing Inquiry" or "Technical Support" = **labeled data** (the category tag IS the label, pairing input with output for supervised learning).

---

## ML Lifecycle

1. **Data ingestion and preparation** — Collecting, cleaning, and transforming raw data into a usable format
2. **Model training** — Creating your ML model using data
3. **Model deployment** — Making a trained model available for use
4. **Model management** — Managing and maintaining models over time

---

## Three Primary ML Learning Approaches

| Approach | How it learns | Example |
|----------|--------------|---------|
| **Supervised learning** | Trains on **labeled data** to predict outputs for new inputs | Email spam classifier trained on labeled spam/not-spam emails |
| **Unsupervised learning** | Uses **unlabeled data** to find natural groupings and patterns | Customer segmentation without pre-defined categories |
| **Reinforcement learning** | Learns through **interaction and feedback** to maximize rewards and minimize penalties | AI robot learning optimal delivery routes via positive/negative scores |

**Key insight from sample exam — Reinforcement learning:**
- Correct answer: "Learning through interaction and feedback"
- The robot story (positive scores for fast delivery, negative for delays) → Reinforcement learning
- NOT supervised (no pre-labeled routes), NOT unsupervised (has a goal), NOT deep learning (that's an architecture, not a paradigm)

---

## Gen AI Landscape: The 5 Layers

| Layer | What it is |
|-------|-----------|
| **Gen-AI-powered application** | The user-facing part — allows users to interact with AI capabilities |
| **Agent** | Software that learns to achieve a goal by observing the world and acting using tools |
| **Platform** | Offers APIs, data management, and model deployment tools — bridges models and agents |
| **Model** | A complex algorithm trained on data; learns patterns and generates new content |
| **Infrastructure** | Core computing resources — servers, GPUs, TPUs, and software for storing/running models |

---

## Google's Foundation Models (Quick Reference)

| Model | What it does |
|-------|-------------|
| **Gemini** | Multimodal: text, images, audio, code — conversational AI, content creation, Q&A |
| **Gemma** | Lightweight, open, customizable — for local deployments and specialized AI apps |
| **Imagen** | Text-to-image diffusion model — generates high-quality images from text descriptions |
| **Veo** | Generates **video** content from text or still images |

**Key insight from sample exam — Imagen vs Veo vs Gemini vs Gemma:**
- Need photorealistic images from text → **Imagen**
- Need video content from text/images → **Veo**
- Need multimodal general understanding → **Gemini**
- Need lightweight open model for local deployment → **Gemma**
- Veo CANNOT process live/fluctuating data streams — it generates video from static inputs

---

## Foundation Model Limitations

| Limitation | Description |
|-----------|-------------|
| **Data dependency** | Performance relies heavily on data quality — biased/incomplete data affects outputs |
| **Knowledge cutoff** | Trained up to a specific date — may lack info about events after that point |
| **Bias** | LLMs learn from large datasets that may contain biases, which can be magnified in outputs |
| **Fairness** | Assessing fairness is a key aspect of responsible development |
| **Hallucinations** | When AI produces outputs that are **not accurate or based on real information** — fabricates convincing but incorrect responses |
| **Edge cases** | Rare and atypical scenarios can expose a model's weaknesses |

**Key insight from sample exam — Hallucinations:**
- AI confidently provides a revenue figure and press release that don't exist = **Hallucinations**
- NOT knowledge cutoff (that would mean saying "I don't know"), NOT bias (that's systematic imbalances), NOT data dependency (that's about quality gaps)

---

## Prompting Basics

**Prompting** — The method of interacting with and guiding foundation models. Involves providing instructions or inputs to generate desired outputs.

**Prompt engineering** — The art and science of creating effective inputs (prompts) for gen AI models to maximize their value and tailor responses to specific needs.

---

## Practice Questions (From Sample Exam)

### Q: A company wants to use LLMs to enhance operations. What is a primary characteristic of LLMs?
**A: LLMs are trained on vast datasets, enabling broad language and context understanding, and adaptability across many tasks.**
- Not singular domain expertise (LLMs are generalist)
- Not small dataset learners
- Not inherently strong logical reasoners without prompting

### Q: An AI robot learns delivery routes via positive/negative scores. What type of ML is this?
**A: Reinforcement learning**
- Reward (positive) + penalty (negative) + environment interaction = reinforcement learning

### Q: A business analyst gets a fabricated revenue figure from an AI. What limitation is this?
**A: Hallucinations**
- The model generates plausible but entirely false information

### Q: Emails tagged "Billing Inquiry" or "Technical Support" — what type of data?
**A: Labeled data**
- Each email has a category tag that serves as a label/output pairing

### Q: What is the definition of a gen AI model?
**A: A complex algorithm trained on vast amounts of data to learn patterns and relationships**
- Not a physical device, not a UI, not a set of rules
