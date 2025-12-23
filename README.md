# Generative AI Design Patterns to deal with common challenges in Production Applications
- Thanks to Valliappa Lakshmanan, Hannes Hapke for the wonderful book https://www.oreilly.com/library/view/generative-ai-design/9798341622654/

## Generative AI / Agentic Applications - Challenges in production
-	Non-deterministic – different answers to same input
-	Hallucinations – confidently generating false or fabricated information
-	Reasoning inconsistencies – Logical errors or contradictions within responses
-	Model customization for an organization / industry – e.g. Medical knowledge or Legal knowledge not present in Foundational Models
-	Context window limitations – Losing important information in long conversations
-	Knowledge cutoff – knowledge till the last trained date of the model

## Design Patterns

We will cover **32 design patterns, organized into eight sections**. You will learn how to control model outputs, enhance knowledge retrieval, improve reasoning capabilities, increase reliability, enable action, optimize performance, and implement safeguards.

### **Controlling Content Style** - We show you how to control the style and format of Al-generated content-which is a critical skill for ensuring brand consistency, accuracy, and compliance.


- **Pattern 1 - Logits Masking** - to ensure that text conforms to specific style rules by intercepting the generation process at the sampling stage.
- **Pattern 2 - Grammar** - will teach you to constrain outputs to specific formats or data schemas using formal grammar specifications.
- **Pattern 3 - Style Transfer** - how to convert content to mimic specific tones through few-shot learning or fine-tuning.
- **Pattern 4 - Reverse Neutralization** - will show you how to generate content in specialized styles by first creating neutral content and then transforming it.
- **Pattern 5 - Content Optimization** - will equip you with methods to determine optimal content styles through systematic comparison and preference tuning-which are particularly valuable for marketing, advertising, and educational materials where effective style factors aren't immediately obvious.



### **Adding Knowledge Base** - You'll learn patterns that can help you build AI systems that leverage external knowledge sources to address fundamental limitations like knowledge cutoffs, confidential data access, and hallucinations.
  - **Pattern 6 - Basic RAG** - learn to ground Al responses in relevant information from knowledge bases.
  - **Pattern 7 - Semantic Indexing** - will teach you to capture meaning across different media types by using embeddings, thus moving beyond simple keyword matching.
  - **Pattern 8 - Indexing at Scale** - you'l1 master techniques for managing outdated or contradictory information through metadata, filtering, and reranking.
  - **Pattern 9 - Index-Aware Retrieval** - will equip you with advanced methods like hypothetical answers, query expansion, and GraphRAG to improve retrieval quality.
  - **Pattern 10 - Node Postprocessing** \- will show you how to handle irrelevant content and ambiguous entities through reranking and contextual compression.
  - **Pattern 11 - Trustworthy Generation** - systems that maintain user trust despite inevitable errors.
  - **Pattern 12 - Deep Search** - will teach you iterative processes for complex information retrieval that overcome context window constraints and enable multi-hop reasoning.



### **Extending Model Capabilities -** we discuss powerful techniques to enhance the reasoning and specialized capabilities of language models.
  - **Pattern 13 - Chain of Thought (CoT)** - which enables models to break down complex problems into intermediate reasoning steps and dramatically improve their performance on mathematical problems and logical deductions.
  - **Pattern 14 - Tree of Thoughts (ToT)** - will teach you to implement tree search approaches for problems requiring exploration of multiple solution paths-which are ideal for strategic thinking and planning tasks.
  - **Pattern 15 - Adapter Tuning** - you'll discover how to efficiently specialize large models by training small add-on neural network layers while keeping original model weights frozen, thus making specialized adaptation practical with limited data (from 100 to 10,000 examples).
  - **Pattern 16 - Evol-Instruct** - will show you how to efficiently generate high-quality instruction-tuning datasets by evolving instructions through multiple iterations, thus enabling you to teach models new domain-specific tasks without extensive manual data creation.



### **Improving Reliability** - you'll encounter patterns for building more reliable Al systems that can be trusted in production environments.
  - **Pattern 17 - LLM-as-Judge** - to evaluate generative AI capabilities through detailed, multidimensional feedback- which is a foundational skill for comparing models and tracking improvements.
  - **Pattern 18 - Reflection** - will teach you how to enable models to correct earlier responses based on feedback, which significantly improves reliability in complex tasks.
  - **Pattern 19 - Dependency Injection** - you'll master techniques for independently developing and testing each component of an LLM chain, thus making your systems more maintainable and robust.
  - **Pattern 20 - Prompt Optimization** - will show you how to systematically set and update prompts by optimizing them on example datasets, which reduces maintenance overhead when dependencies change and ensures consistent performance over time.



### **Enabling Agents to take action** - we discuss ways to transform your AI systems from passive information providers into active agents that can take meaningful actions in the world.
  - **Pattern 21 - Tool Calling** - to learn how to bridge LLMs with software APIs so they can invoke functions with appropriate parameters and incorporate the results into their responses. This enables real-time data access, connections to enterprise systems, and complex calculations.
  - **Pattern 22 - Code Execution** - will teach you to leverage LLMs to generate code that can be executed by external systems-which is perfect for creating visualizations, annotating images, or updating databases.
  - **Pattern 23 - Multiagent Collaboration** - you'll learn to design systems of specialized single-purpose agents that are organized in ways that mimic human organizational structures, thus enabling complex reasoning, multistep problem solving, collaborative content creation, and self-improving systems that can handle extended interactions without human intervention.



### **Addressing Constraints** - you'll learn essential patterns for deploying generative Al within real-world constraints of cost, latency, and computational resources.
  - **Pattern 24 - Small Language Model (SLM)** \- will demonstrate how to leverage smaller, more efficient models that can run on edge devices or with limited resources while still delivering acceptable performance for specific tasks.
  - **Pattern 25 - Prompt Caching** - you'll discover techniques to reduce redundant computations and API calls and thus significantly lower costs for frequently requested content.
  - **Pattern 26 - Inference Optimization** - will equip you with methods to maximize throughput and minimize latency through techniques like speculative decoding, continuous batching, and prompt compression.
  - **Pattern 27 - Degradation Testing** - will show you how to systematically evaluate model performance across different deployment scenarios and thus ensure consistent quality over time.
  - **Pattern 28 - Long-Term Memory** - will demonstrate how to maintain user history and dynamically apply personalization.



### **Setting Safeguards** - will equip you with critical patterns for ensuring your generative Al applications operate safely, ethically, and within appropriate boundaries.
  - **Pattern 29 - Template Generation** - will teach you how to pre-generate and review templates that require only deterministic string replacement at inference time- which is ideal for high-volume personalized communications where human review isn't scalable.
  - **Pattern 30 - Assembled Reformat** - you'll learn to separate content creation into low-risk steps: first assembling data safely and then formatting it attractively to reduce the risk of inaccurate or hallucinated content.
  - **Pattern 31 - Self-Check** - will show you how to use token probabilities to detect potential hallucinations cost-effectively in factual responses.
  - **Pattern 32 - Guardrails** \- will equip you with comprehensive approaches to wrapping LLM calls with preprocessing and postprocessing layers that enforce security, privacy, content moderation, and alignment constraints-which is essential whenever your application could face malicious adversaries.



### **Production ready Agentic application** - Finally we will demonstrate how the key patterns can be composed into a production-ready agentic application.