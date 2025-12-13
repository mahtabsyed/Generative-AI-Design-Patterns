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
### Controlling Content Style (Patterns 1-5)
1. Logits Masking - Need to ensure generated text conforms to specific style rules for brand, accuracy, or compliance reasons.
2. Grammar - Need text to conform to a specific format or data schema for downstream processing.
3. Style Transfer - Need to convert content into a form that mimics specific tone and style that is difficult to express through rules, but can be shown through example conversions.
4. Reverse Neutralization - Need to generate content in a specific style that can be shown through example content.
5. Content Optimization - Need to determine optimal style for content without knowing which factors matter.

### Adding Knowledge (Patterns 6-12)


### Extending Model Capabilities (Patterns 13-16)


### Improving Reliability (Patterns 17-20)


### Enabling Agents to Take Action (Patterns 21-23)


### Addressing Constraints (Patterns 24-28)


### Setting Safeguards (Patterns 29-32)
