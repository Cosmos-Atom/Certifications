# Section 4: Business Strategies for a Successful Gen AI Solution
**~15% of the exam**

---

## Before Starting Your Gen AI Project

Two things to assess: **Needs** and **Resources**

### Needs
| Factor | Question to ask |
|--------|----------------|
| **Scale** | How many users will there be? |
| **Customization** | How specialized is this AI? |
| **User interaction** | How will users engage? |
| **Privacy** | How sensitive is the data? |
| **Latency** | What response time can you have? |
| **Connectivity** | What is your connectivity? |

### Resources
| Factor | Question to ask |
|--------|----------------|
| **People** | Do you have access to AI expertise? |
| **Money** | What's your budget? |
| **Time** | What are your project timelines? |

---

## Gen AI Strategy Framework

Use a **combined top-down and bottom-up approach**:
- **Top-down** — Leadership sets the vision and strategy
- **Bottom-up** — Employees identify practical applications and provide feedback

### Six Strategic Pillars

| Pillar | What it means |
|--------|--------------|
| **Strategic focus** | Prioritize focused gen AI implementations with clear business value |
| **Exploration** | Encourage experimentation and collaboration to discover valuable gen AI applications |
| **Responsible AI** | Establish ethical guidelines and ensure secure and responsible AI development |
| **Resourcing** | Invest in data strategy, leverage existing resources, and develop AI talent |
| **Impact** | Measure gen AI's impact on business goals and demonstrate tangible benefits |
| **Continuous improvement** | Continuously refine gen AI solutions based on feedback and data |

---

## Responsible AI

**Responsible AI** — Ensuring your AI applications don't cause harm and are used in an ethical manner.

- Responsible AI must be considered throughout the **entire AI lifecycle**: data preparation, model training, deployment, and ongoing monitoring
- It's not a one-time checkbox — it's a continuous process

### Key Principles in Practice
- **Transparency** — Users need to understand how AI systems make decisions
- **Explainability** — Making AI decision-making processes understandable and accountable
- **Fairness** — Assessing the fairness of gen AI models is a key aspect of responsible development
- **Ethics** — Establishing ethical guidelines for AI use

**Key insight from sample exam:** HR department uses a gen AI model to screen job applications. Qualified candidates are overlooked but the AI provides no explanation. The company needs to address the **lack of transparency**. → **Implement explainable gen AI policies**. Explainable AI directly tackles unclear decision-making, making the AI's ranking factors transparent and understandable.

- NOT collect a larger dataset (improves accuracy but doesn't make the screening process transparent)
- NOT fine-tune the model (improves performance but doesn't reveal how decisions are made)
- NOT develop fairness assessments (identifies biases but doesn't explain individual candidate rankings)

---

## Secure AI

**Secure AI** — Protecting your AI applications from harm.

### Secure AI Framework (SAIF)
The **Secure AI Framework (SAIF)** helps organizations manage AI/ML model risks and ensure security.

Google Cloud's secure-by-design infrastructure supports security across the AI/ML lifecycle.

### Key Security Tools

| Tool | Purpose |
|------|---------|
| **Identity and Access Management (IAM)** | Controlling resource access |
| **Security Command Center** | Security posture visibility |
| **Workload monitoring tools** | Build and maintain secure AI systems |

---

## Factors When Choosing a Model for Your Use Case

| Factor | What to consider |
|--------|-----------------|
| **Modality** | Choose a model whose input/output data types align with your needs (text, images, audio, video) |
| **Context window** | Balance ability to generate coherent responses against increased computational costs |
| **Performance** | Accuracy, speed, and efficiency — consider the trade-offs between performance and cost |
| **Availability and reliability** | Consistently available, performs reliably under load — uptime guarantees, redundancy, disaster recovery |

---

## Planning for Your Gen AI Strategy

To plan for your gen AI strategy, establish:
1. A **clear vision**
2. **Prioritize use cases**
3. Invest in **capabilities**
4. **Manage change**
5. **Measure value**
6. **Champion Responsible AI**

---

## Responsible AI Throughout the AI Lifecycle

| Stage | What responsible AI looks like |
|-------|-------------------------------|
| **Data preparation** | Use diverse, unbiased, representative data |
| **Model training** | Monitor for bias and fairness; document training choices |
| **Deployment** | Implement explainability; set up human-in-the-loop where needed |
| **Ongoing monitoring** | Drift monitoring, performance tracking, fairness audits |

---

## Key Business Concepts Tested

### Explainable AI
- Makes AI decision-making processes **transparent and understandable**
- Crucial for building trust and identifying potential issues
- Required in high-stakes applications (HR, healthcare, finance, legal)

### Democratizing AI
- Making AI accessible to organizations regardless of technical expertise
- Google Cloud approach: low-code/no-code tools + pre-trained models + easy-to-use APIs
- Empowers individuals with different technical backgrounds

### Vendor Lock-in vs. Open Approach
- **Vendor lock-in concern** → Google Cloud's **open approach** is the answer
- Open standards allow services to move between vendors
- Proprietary = lock-in, Open = flexibility

---

## Practice Questions (From Sample Exam)

### Q: HR department uses gen AI to screen job applications. Qualified candidates are overlooked but the AI provides no explanation. What should they do?
**A: Implement explainable gen AI policies**
- Explainable AI makes the factors the model uses to rank/exclude candidates transparent and understandable
- Larger/diverse dataset = doesn't make the screening transparent
- Fine-tuning = improves performance, doesn't reveal how decisions are made
- Fairness assessments = identifies biases but doesn't explain individual candidate rankings or exclusions

---

## Cheat Sheet: Picking the Right Google Cloud Tool

| Business Need | Right Tool |
|---------------|-----------|
| Quick personal productivity chatbot | Gemini app |
| Analyze multiple research documents | Gemini Notebook |
| Internal knowledge base for employees | Gemini Enterprise |
| Unified contact center (phone/email/chat) | CCaaS (Contact Center as a Service) |
| Central ML platform (build/deploy/monitor) | Gemini Enterprise Agent Platform |
| Quick AI prototyping | Google AI Studio |
| Production-ready AI apps | Agent Studio |
| Search over structured/unstructured data | Agent Search |
| Generate high-quality images from text | Imagen |
| Generate video from text or still images | Veo |
| Multimodal AI (text/image/audio/code) | Gemini |
| Lightweight model for local deployment | Gemma |
| Deploy AI on edge devices | Gemini Nano + LiteRT |
| Content without setup/prebuilt tool | Gemini app |
| Brand-consistent, personalized AI assistant | Gem (within Gemini) |

---

## Cheat Sheet: When Models Can't Help — Use These Techniques

| Problem | Solution |
|---------|---------|
| AI gives outdated answers | Grounding / RAG |
| AI hallucinates facts | Grounding (connect to verified sources) |
| AI doesn't know about new features | RAG (retrieve from product docs) |
| Need AI tuned for specific domain | Fine-tuning |
| Need transparent AI decisions | Explainable AI / Responsible AI policies |
| High-stakes decisions need human oversight | Human-in-the-loop (HITL) |
| AI response is too random/creative | Lower temperature |
| Need to give AI a persona | Role prompting |
| AI needs examples to follow | Few-shot prompting |
