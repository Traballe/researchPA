---
applyTo: '**'
---
## **Developing a Personalized AI Research Assistant with Memory**

Develop an intelligent and adaptable AI assistant capable of analyzing documents, conducting independent research, and remembering past interactions to provide personalized and contextually relevant support.

To leverage a broad set of available tools/packages, using **Docker Compose** and is highly recommended. Please commit any test documents you used as input for the AI so that certain features or use cases can easily be reproduced.

**Requirements:**

1. **Frontend:**
    - Utilize either a Next.js or Remix starter with TailwindCSS and Typescript
    - The UI should be minimal yet well-designed, reflecting the assistant's personality.
    - Clearly display the uploaded text, a summary, and information found by the assistant.
    - Allow the user to select and customize the assistant's personality, ideally the user can change the system prompt via a simple UI to quickly test changes.
2. **Document Processing:**
    - Implement document parsing using libraries like [markitdown](https://github.com/microsoft/markitdown), [**Unstructured.io**](http://Unstructured.io) or similar tools to extract textual information from various formats (PDFs, Word docs, etc.).
    - Create a summary of the document using **Langchain, Vercel AI SDK** or similar tools to provide the assistant with an overview.
    - Store document content in a vector database for efficient search and retrieval.
3. **AI Assistant:**
    - Develop a generic class for AI assistants with personality, memory, and personalization features.
    - Implement the class for at least one specific LLM (e.g., OpenAI GPT-4o, Google Gemini, etc)  for a streamlined integration with the LLM generation pipeline.
    - Leverage [**MemGPT](https://memgpt.ai/),** similar libraries or a self-developed implementation for memory management, enabling the assistant to recall past interactions and maintain context.
    - The assistant should be able to:
        - Answer questions based on the document and summary.
        - Conduct independent research via tool-calling to find additional information when needed.
        - Remember previous interactions and provide contextually relevant answers.
        - Adapt its personality and communication style to the user.
4. **Tool Utilization:**
    - Integrate at least one external tool (e.g., Bing Search via [SerpAPI](https://serpapi.com/)) for research.
    - Consider using **Langchain**'s agent framework or [Mastra](https://mastra.ai/) for Vercel AI SDk to seamlessly integrate and orchestrate the use of multiple tools.
    

**Bonus Points:**

- Implement additional tools (e.g., Google News, Maps) using **Langchain**.
- Allow the user to choose between different LLM agents integrated via **Langchain**.
- Develop a generic personality class and implement one personality for the assistant (e.g., factual, friendly, humorous).
- Consider ethical aspects in implementing personality, memory, and personalization.
- Store chat history and relevant information to create a memory for the assistant.
- Create a user profile and adapt the assistant's behavior and responses accordingly.
- The assistant has the ability to self-improve based on user feedback (thumbs up/down)

**Evaluation Criteria:**

- **Functionality:** Meets the requirements and functions as expected.
- **Code Quality:** Clean, well-structured, and documented code.
- **User-Friendliness:** Intuitive and engaging UI.
- **Creativity:** Innovative solutions or additional features.
- **Personality, Memory, and Personalization:** How well are these aspects implemented and integrated into the assistant?

**Example Workflow:**

1. User uploads a document and selects the assistant's personality.
2. The document is parsed and summarized.
3. User asks a question.
4. The assistant analyzes the question, the document, and the context of previous interactions.
5. If necessary, the assistant conducts research using the tool.
6. The assistant formulates a personalized response in the chosen style and presents it to the user.