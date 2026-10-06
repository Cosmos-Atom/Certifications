# Section 3: Techniques to Improve Generative AI Model Output
**~20% of the exam**

---

## Prompting Techniques

**Prompting** — Providing instructions or inputs to guide a gen AI model to generate desired outputs.

### Basic Prompt Types

| Technique | Description |
|-----------|-------------|
| **Zero-shot** | Asking the model to complete a task with **no prior examples** |
| **One-shot** | Providing the model with **one example** to learn from |
| **Few-shot** | Giving the model **multiple examples** to learn from |
| **Role** | Assigning a persona to the model to influence its style, tone, and focus |
| **Prompt chaining** | Engaging in a back-and-forth conversation with the AI to refine and build outputs |

### Advanced / Reasoning Loop Techniques

| Technique | Description |
|-----------|-------------|
| **ReAct (reason and act)** | Allows the LLM to reason and take action on a user query — good for agents |
| **CoT (chain-of-thought)** | Guides an LLM through a problem-solving process by providing examples with intermediate reasoning steps |
| **Metaprompting** | Using prompting to guide the AI model to generate, modify, or interpret other prompts |

---

## Streamlining Prompting Workflows

| Method | How |
|--------|-----|
| **Reusing prompts** | Save prompts as templates for repeated use |
| **Prompt chaining** | Continue conversations within the same chatbot to maintain context |
| **Saved info in Gemini** | Store specific information for the model to use consistently |
| **Gems** | Personalized AI assistants within Gemini — provide tailored responses to specific instructions; streamline workflows via templates, prompts, and guided interactions |

---

## Model Guidance and Refinement

### Grounding
**Grounding** — Connecting the AI's output to **verifiable sources of information**.

- Prevents hallucinations by anchoring responses to real, verifiable data
- Example: connecting a gen AI tool to the latest internal policy documents so it gives accurate, up-to-date answers

**Key insight from sample exam:** A gen AI policy tool is giving outdated/inaccurate information. Company wants reliable answers based on latest official documents. What should they do? → **Implement grounding techniques**. Grounding connects the AI's output to verifiable information sources like internal documents. NOT fine-tuning with broader general knowledge (doesn't ensure adherence to specific internal policies), NOT increasing temperature (would increase inaccuracy), NOT reducing token count (only affects response length, not accuracy).

---

### Retrieval-Augmented Generation (RAG)

RAG is a specific **grounding method** that retrieves relevant information before generating a response.

**RAG Process:**
1. **Retrieval** — The LLM retrieves relevant information from external sources using tooling
2. **Augmentation** — The retrieved information is incorporated into the prompt to the LLM
3. **Generation** — The LLM processes the prompt and generates a response
4. **Iteration (optional)** — The LLM can iterate on the retrieval process as necessary

**Architecture:** Prompt → Model → Query → Vector DBs → Output

**When to use RAG vs alternatives:**
| Need | Solution |
|------|---------|
| Access latest info without retraining | **RAG** |
| Improve model on task-specific performance | Fine-tuning |
| Guide model behavior | Prompt engineering |
| Human review of sensitive outputs | HITL |

**Key insight from sample exam:** Software company chatbot can't answer questions about recently released features (info not in training data). Want to use latest product documentation without retraining the entire model. → **Retrieval-Augmented Generation (RAG)**. RAG allows the LLM to retrieve relevant information from external sources (like latest product documentation) to generate accurate responses. NOT fine-tuning (requires retraining — time-consuming), NOT prompt engineering alone (can't provide info model doesn't have), NOT HITL (requires human intervention, doesn't automatically enable the chatbot).

---

## Sampling Parameters

Settings that influence the AI model's behavior for customized results.

| Parameter | What it controls |
|-----------|-----------------|
| **Token count** | Meaningful chunks of text (words and punctuation) — affects response length |
| **Temperature** | Controls "creativity" or randomness of word choices during text generation — higher = more creative/random |
| **Top-p (nucleus sampling)** | Cumulative probability of most likely tokens considered — another way to control randomness |
| **Safety settings** | Filter out potentially harmful or inappropriate content from model output |
| **Output length** | Determines maximum length of generated text |

**Key insight:** Increasing temperature → **more random/inaccurate** responses. If you want more reliable responses, decrease temperature. Reducing token count only affects response length, not accuracy.

---

## Foundation Model Limitations (Review)

| Limitation | What it means in practice |
|-----------|--------------------------|
| **Data dependency** | Biased or incomplete training data affects outputs — garbage in, garbage out |
| **Knowledge cutoff** | Model doesn't know about events after its training date |
| **Bias** | Training data biases can be amplified in outputs |
| **Fairness** | Need to actively assess model fairness throughout development |
| **Hallucinations** | Model fabricates convincing but false information |
| **Edge cases** | Rare scenarios expose model weaknesses |

---

## Human-in-the-Loop (HITL)

A process where **human input and feedback are directly integrated into ML workflows**.

### When HITL is critical:

| Use case | Why |
|---------|-----|
| **Content moderation** | Ensures user-generated content is moderated contextually, catching harmful material algorithms might overlook |
| **Sensitive applications** | Healthcare and finance require critical oversight for accuracy and risk reduction |
| **High-risk decision-making** | Safeguards accuracy and accountability through human review of ML outputs |
| **Pre-generation review** | Human experts validate ML outputs before deployment, catching errors or biases |
| **Post-generation review** | Continuous feedback after deployment helps models improve and adapt |

---

## Managing Your Model

Google Cloud offers tools for managing the entire ML lifecycle:

| Tool/Practice | What it does |
|--------------|-------------|
| **Versioning** | Keep track of different versions with Model Registry |
| **Performance tracking** | Review model metrics to check performance |
| **Drift monitoring** | Watch for changes in model accuracy over time with Model Monitoring |
| **Data management** | Use Agent Platform Feature Store to manage data features |
| **Storage** | Use Model Garden to store and organize models |
| **Automate** | Use Agent Platform Pipelines to automate ML tasks |

---

## Additional Key Terms

| Term | Definition |
|------|-----------|
| **Context window** | The amount of text the model can consider at one time |
| **Fine-tuning** | A technique to enhance a pre-trained/foundation model's performance for specific tasks or domains — requires retraining |
| **Grounding** | Connecting AI output to verifiable sources |
| **RAG** | Retrieval-Augmented Generation — retrieve → augment → generate |

---

## Fine-tuning vs RAG vs Prompt Engineering

| Technique | When to use | Key difference |
|-----------|-------------|----------------|
| **Fine-tuning** | Need model to internalize a new skill/style | Requires retraining — time and compute intensive |
| **RAG** | Need access to fresh/external knowledge | No retraining — retrieves at query time |
| **Prompt engineering** | Need to guide behavior within existing knowledge | No retraining — works with what the model knows |
| **Grounding** | Need reliable, verifiable, factual answers | Connects output to authoritative sources |

---

## Practice Questions (From Sample Exam)

### Q: Software company chatbot can't answer questions about recently released features without retraining. Which technique?
**A: Retrieval-Augmented Generation (RAG)**
- RAG allows the LLM to retrieve relevant information from external sources (latest product documentation)
- Fine-tuning requires full retraining
- Prompt engineering can't access info the model doesn't have
- HITL requires human intervention, doesn't enable the chatbot automatically

### Q: A gen AI policy tool gives outdated/inaccurate information. What should the organization do to give reliable answers based on latest official documents?
**A: Implement grounding techniques**
- Grounding connects AI output to verifiable information sources like internal documents
- Fine-tuning with broader general knowledge won't ensure adherence to specific internal policies
- Increasing temperature would increase inaccuracy
- Reducing token count only affects response length
