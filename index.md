# Digital Bouncers

## Introduction
In “The great acceleration: CIO perspectives on generative AI” by the MIT Tech Review and
Databricks, Schaefer—Chief Health Informatics Officer at Kansas City VA Medical Center—
stated “trust” as the Key to effectively adopting generative AI. The healthcare industry is
a great case study for involving a multitude of high-stake processes and parties, such as
the use of machine learning models to predict protein structures, assist drug discovery,
and track the progression of outbreaks, to chatbots helping front-line staff by transcribing
medical notes and answering patients’ questions. The same understanding of such broad
applications can be applied to other areas, including a smart home chatbot, where privacy
concerns are prominent as users decide who gets to use their data, which data, and for what
purposes. As more rooms and appliances generate data in homes, the “democratization”
of data control and ownership is poised to gain traction to build “trust” in generative AI.
The reverse also applies as developers aim to protect the integrity of AI systems by mod-
erating which user inquiries to accept or reject. Meeting these expectations requires the
effective and ethical implementation of conversational AI to protect data and systems in-
tegrity, safety, and privacy for the collective benefits of those affected most by generative
AI.

### What are guardrails?
Explain what are guardrails

### Background and Oppurtunity
Many prominent works have been done to document, understand, and disseminate the risks
and threats of generative AI, notably is the OWASP Top 10 security risks for large language
model (LLM) applications, which includes prompt injection, insecure output handling, sen-
sitive information leakage, excessive agency, to model theft. Knowing these preeminent
threats allows developers and users of LLM-based chatbots to navigate development envi-
ronments, workflows, usage, and system architectures with proactive risk-mitigation tech-
niques to address these concerns. Several legislations worldwide have been adopted to
protect data integrity and privacy through “data minimization” best practices for transmis-
sion, storage, and API-intensive AI workflows, including the EU’s General Data Protection
Regulation (GDPR) in Article 5(1)(c), and the California Privacy Rights Act (CPRA) in Cal.
Civ. Code § 1798.100 (d). It is critical for current and future developers of AI systems to
take leadership and proactive steps in implementing best data-handling practices to inspire
a future of safe and secure digital interactions with “digital bouncers”.

## Our Solution
Digital Bouncers aims to address these concerns with an LLM-based resource-use moni-
toring chat application with AI risk-mitigation for physical assets – a trustworthy assistant
3
users can rely on to ask general questions about smart home energy use. By building upon
existing LLM guardrails, our application hopes to demonstrate a feasible solution through
guardrails to common problems in LLM applications at the input, intermediary, and output
level.
In terms of our actual chat bot application, we incorporated two main features/workflows:
- For questions that can be answered by performing SQL on the dataset, we’ve imple-
mented a Text2SQL pipeline that utilizes Langchain agents to perform the necessary SQL
operations on the data.
- For other questions that cannot be answered using SQL, we call a separate general
LLM model that answers the question.
As mentioned earlier, we also focus on implementing guardrails to provide a flawless and se-
cure user experience. Below we give a general overview of the guardrails we used through-
out the workflow, as well as the problem they guarded against.
- Input Moderation Guardrail: We have a guardrail at the input level that guards against
of topic prompts, as well as harmful or inappropriate prompts.
- Intermediary Guardrail: Since we have two main workflows in the Text2SQL and
general LLM; we have an intermediary guardrail that determines which workflow to use
according to the question asked.
- RAG Check Guardrail: We have a RAG evaluation guardrail that checks whether or
not the answer given makes logical sense. Sort of a sanity check on the output response of
our chat bot if you will.
- Output Moderation Guardrail: We will have a guardrail blocks/rewrites responses to
conform to our predefined guidelines. This guardrail will also perform a basic syntax check.
In summary, our goal is to provide users with secured recommendations regarding smart
home utility bills. We aim to facilitate private, safe, and secure interactions between LLMs
and users with robust guardrails and thoughtful interaction flow design that addresses the
prevalent risks of conversational AI.

### LLM/RAG
Dives into the LLM/RAG component of our project (such as text2sql)

### Guardrails
Dives into the different guardrails used for our product and why

### LangGraph Persistence Layer
Elaborates on the LangGraph Persistence Layer for our product

## Example Prompts
This section evaluates the performance of our chatbot on different inputs, as well as the performance of our implemented guardrails

### Input Guardrail

### Text2SQL Guardrail

### RAG Evaluation Guardrail

### Output Guardrail

## Results
Talk about the results of our chat bot on given tests

## Additional Links
Section to check out our actual source code, and report. (maybe move it to the top of the page)
