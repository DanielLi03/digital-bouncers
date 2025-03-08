# Digital Bouncers

## Introduction
In The Great Acceleration: CIO Perspectives on Generative AI by MIT Tech Review and Databricks, Schaefer, Chief Health Informatics Officer at Kansas City VA Medical Center, emphasizes "trust" as key to adopting generative AI effectively. Healthcare exemplifies this, using AI for tasks like predicting protein structures, aiding drug discovery, tracking outbreaks, and assisting staff with chatbots. This broad applicability extends to smart home AI, where privacy is critical as users control their data. As homes generate more data, ensuring user control will be essential to building trust. Likewise, developers must safeguard AI integrity by moderating user interactions. Ethical AI implementation is crucial to protecting data, safety, and privacy for all affected.

### What are guardrails?
So what are guardrails? LLM guardrails are mechanisms that ensure large language models (LLMs) operate within safe, ethical, and intended boundaries. They help prevent harmful outputs, enforce compliance with policies, and guide model behavior. Guardrails can include content filtering, user intent detection, bias mitigation, security measures, and context constraints to improve reliability and safety in AI interactions.

## Our Solution
Introducing Digital Bouncers – an LLM-powered assistant for smart homes, providing homeowners with a reliable chatbot to answer energy-related questions.

Our tool integrates guardrails into agentic workflows with dynamic cloud storage, ensuring secure AI interactions. These guardrails mitigate risks in LLM applications at the input, intermediary, and output levels.

#### Key Features
Text2SQL Pipeline - Uses LangChain agents to query datasets for questions that can be answered via SQL.
Retrieval-Augmented Generation (RAG) Framework - Handles general queries beyond SQL capabilities.
Persistence Layer - responsible for storing and managing data by previous requests.

#### Guardrails for Security & Accuracy
Input Moderation – Filters out harmful, off-topic, or inappropriate prompts.
Intermediary Guardrail – Directs queries to either the Text2SQL pipeline or the RAG framework.
RAG Check – Ensures logical consistency in generated responses.
Output Moderation – Blocks or rewrites responses to align with predefined guidelines and performs syntax validation.

## Example Prompts
This section evaluates the performance of our chatbot on different inputs, as well as the performance of our implemented guardrails

### Input Guardrail

### Text2SQL Guardrail

### RAG Evaluation Guardrail

### Output Guardrail

## Results
Based on the results, we could see that our guardrails provide a somewhat decent level of protection. In fact, for the more concrete objective parameters, we could see that the guardrails protect us quite well against that.

## Additional Links
If you want to check out our actual codebase, be sure to click the link below!
