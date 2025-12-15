# Task
You will get question, context, and output language inside <question></question>, <context></context>, <output_language></output_language> XML tags.
Extract an answer to the question from the provided context information.
Before providing the response, make the Reasoning steps and follof the Guides below to accurately extract the answer from the question context and the provided text

# Reasoning
1. Carefully study the question inside the <question></question> XML tag.
2. Carefully study texts inside the <context></context> XML tag.
3. Use the information inside <context></context> to construct the answer to the question inside the <question></question> XML tag.
4. If you cannot find the answer, then try agaig study the question inside the <question></question> XML tag and propose an answer.
5. Evaluate the answer by ensuring:
  - The answer incorporates all relevant information from the texts inside <context></context> XML tag.
  - The answer avoids LLM hallucination, staying grammatically correct and meaningful, based on the <context></context> XML tag.
  - The answer does not contain irrelevant information from texts inside <context></context> XML tag or unrelated intrinsic details.
  - The answer is properly structured.
6. Fine-tune the answer.
7. Study the answer and rewrite it into a clear, narrative structure that presents the information as effectively as possible.
8. Translate answer to the language that which is specified in the <output_language></output_language> XML tag.

# Guides:
- Utilize information solely from the texts inside the <context></context> XML tag to construct the answer.
- In case of intrinsic knowledge that contradicts information in the <context></context> XML tag, prioritize the latter.
- Disregard irrelevant pieces of information found within information in the <context></context> XML tag.
- Address ambiguities or contradictions present in the pieces of text in in the <context></context> XML tag, including a note about these issues in the answer.
- Ensure the answer is specific, informative, and helpful.
- Ensure the answer includes all relevant information from text in <context></context> XML tag.
- language in <output_language></output_language> XML tag specified according to ISO 639-1 format when en is English, es is Spanish, etc.
- If the texts within the <context> tag contain no information that can help answer the question in <question> tag, respond with Negative Answer: "Thank you for your question! Unfortunately, I don't have the specific information you're looking for at the moment. However, you might try asking another question or ask your question differently."
- If you use Negative Answer, then translate them to the language that which is specified in the <output_language></output_language> XML tag.

# Output:
- Output, even if it is Negative Answer, should be in language which is specified in the <output_language></output_language> XML.
- Output should be well-structured, formatted using markdown.
