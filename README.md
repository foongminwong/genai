# Generative AI

Resources:
[How to Fast Track your Generative AI Knowledge and Expertise in two hours / | Andrew Larkin](https://www.linkedin.com/posts/larky_what-is-generative-ai-course-cloud-academy-activity-7122442798275985408-HS1X)

1. [What is Generative AI?](https://platform.qa.com/course/what-generative-ai-4856/an-introduction-to-generative-ai/)
- OpenAI built technologies with AI models that can take natural language input from a user and return a machine-created human-like response.
- Summarize text, provide code suggestions, generate images for a website, etc.
- Generative Pre-trained Transformer (GPT)
    - Understand & create natural language
    - Take an input, or prompt, and returns a natural language, visual, or code response
- AI (Imitate human behavior by relying on machines to learn and execute tasks without explicit directions on what to output) -> Machine Learning (Algorithms take in data and fit models to the data to make predictions) -> Deep Learning Models (Use layers of algorithms in the form of artificial neural networks, for more complex use cases)
- Many Azure AI services are built on deep learning models.

2. [Introduction to Large Language Models](https://platform.qa.com/course/introduction-large-language-models-4683/introduction-1725534386421/)

a. Introduction to Large Language Models
- Large Language Model (LLM) -  A type of machine learning model specifically designed for processing and generating text.
- A highly sophisticated chatbots with the ability to “understand” and produce content on a wide range of topics.
- LLMs don't genuinely understand, reason, or think. They are AI, but they don't have intrinsic intelligence.
- In the realm of LLMs, 
    - "Understanding":  It refers to the model's ability to accept input and accurately predict output.
    - "Learning": It refers to the adjustments made to the model's parameters which influence its predictions.
- LLMs consume text-based input referred to as a prompt and produce relevant output.
- ChatGPT - A chatbot built on top of some of the more advanced LLMs
- LLM Use Cases:
    - Content Generation
    - Code Generation
    - Education and Tutoring
    - Research
    - Customer Support
    - Entertainment
        - Used in on-player characters (NPCs) in video games to produce more realistic dialogues and behaviors.
        - Produce interactive stories with adaptive branching narratives that change in response to user input.
    - Productivity Tools
    - Translation and Localization
    - Accessibility
    - Programming Assistance
    - Business Intelligence
    - Healthcare
    - Social Media Monitoring
- LLM Limitations:
    - Time consuming & expensive to keep LLMs up-to-date with current information. Lack any knowledge available after the date on which they were trained.
    - Self-contained. No ability to perform external actions other than responding to a single prompt. Requires external tooling and custom development to enable LLM-driven applications to extend beyond the isolation.
    - Constrained by the total amount of input and output - potential for stale information, I/O constraints limit the amount of contextual information provided inside of prompts.
    - Can make mistakes and reflect biased opinions since they are only as good as the data on which they’re trained. 
    - Designed to produce output based on a prompt even if they lack the knowledge to respond to the prompt

b. How Do Large Language Models Work?
- LLM: 
    - A particular type of artificial neural networks known as deep learning models. These models consist of layers of interconnected nodes – analogous to neurons – that can "learn" patterns from data.
    - Trained on vast amounts of text-based data. Data is taken from books, articles, websites, and other sources of written content
    - “Learn” the structure of the language, common phrases, facts, reasoning abilities, and even some cultural nuances. 
    - They are presented with snippets of text and try to predict the next word in the sequence.
- LLM Training:
    - During training, models identify relationships between words.
    - Example: 'apple" is often associated with the words "fruit" and "phone."
    - These relationships are stored as weights in a neural network, which can have billions of parameters. 
    - GPT-3: 175 billion parameters. 
    - GPT-4 series models:  ~1.75 trillion paramters.
- LLM Architecture:
    - "Transformer" 
    - Transformers represent the “T” in ChatGPT. Which holistically stands for “Generative Pre-trained Transformer.” 
    - "Attention Mechanism": Key component of the Transformer, allows the model to focus on different parts of the input text when producing an output.
        - Pay attention to the words most important to the main ideas while reading a long article
        - Weighs parts of the input differently to generate an appropriate output.
- LLM Tokenization:
    - Models do not technically operate on words in the same way as humans. They operate on tokens, which are often words or sub-words/ word fragments. 
    - Before input is provided to models, it goes through a process called tokenization.
    - Break down words into smaller chunks, especially for languages with compound or uncommon words.
    - "unbelievable" ->  “un” and “believable”
- How LLM works:
    - Predict the next logical sequence of tokens. 
    - Example: Input: "The sky is...", Next token prediction: "Blue."
    - "Context Window"
        - Constrained by the amount of input and output tokens
        - Determines the maximum number of tokens an LLM can consider at once, from both the input and the output combined. 
        - Input exceeding this limit may lose the beginning of the text, potentially losing critical information. This limitation emphasizes the importance of concise and relevant input, especially in longer interactions. 
- LLM Terms:
    - "Temperature": 
        - A floating point number that ranges between 0 and 1.
        - Control and tune the LLMs to produce outputs that vary in randomness when generating texts 
        - Low temperature: more deterministic & consistent  results
        - High temperature: more random & creative results.
    - "Prompts":
        - Initial input you provide to the model.
        - Sets the stage for the expected type of response. 
        - A well-crafted prompt can guide the model to produce more accurate or contextually relevant responses.
    - "Sampling":
        -  How the model chooses the next word (or token) in the sequence. At each step, the model produces a distribution of probabilities for the next token. 
        - Determine how the model selects from these probabilities. 
        - Sampling methods: 
            - Greedy Sampling: Chooses the word with the highest probability. Temperature doesn't affect greedy sampling because there's no randomness involved.
            - Random Sampling:
                - Next word is chosen based on its probability distribution. Temperature plays a direct role in shaping this distribution.
                - A high temperature makes the distribution flatter, introducing more randomness.- A low temperature sharpens the distribution, making the output more deterministic.
            - Top-k Sampling: Select from the top k most probable words. Within this subset, temperature can adjust how probabilities are distributed.
            - Top-p (Nucleus) Sampling: Pick words from a subset that cumulatively exceeds a probability threshold p. Again, within this subset, temperature can influence individual word probabilities.
- LLM Model Fine-tuning:
    - Specialize them for particular tasks
    - Training the model further on a narrower dataset, allowing it to become an expert in specific domains or adapt to specific styles.
    -  Extend the value of older models, bringing their efficacy up to comparable levels of newer, more expensive models. 
    - Reduce the amount of required prompt input, by codifying behaviors directly into the model. 
c. Knowledge Check:
    - Q1: How do large language models (LLMs) like ChatGPT learn language patterns and nuances? 
        - A1: They are trained on vast amounts of text-based data and adjust their internal parameters through prediction.
        - E1: LLMs are trained on extensive datasets containing text from books, articles, websites, and other written sources. During training, they adjust their internal parameters by predicting the next word in a sequence of text. Incorrect predictions result in parameter adjustments, allowing the model to become proficient at generating text based on the patterns it has learned.
    - Q2: What is the primary purpose of large language models (LLMs) like ChatGPT?
        - A2: To generate text-based content on a wide range of topics.
        - E2: Large language models do not possess the ability to think, reason, or genuinely understand. Their primary function is to generate the next logical sequence of tokens based on the provided input prompt. Although LLMs can be incorporated into applications to execute external actions, this is not the primary purpose of the underlying model. While medical diagnostics can be one of the potential use cases for LLMs, it is not their primary function.
    - Q3: What role does "temperature" play in controlling the output of LLMs?
        - A3: It influences the randomness of word choice in generated text.
        - E3: Temperature is a parameter that affects the randomness of word choice in generated text. A higher temperature value produces more random and creative results, while a lower temperature value leads to more deterministic and focused text generation.
    - Q4: There are many ethical concerns related to the LLMs.Which of the following use cases have the highest probability of causing people harm?
        - A4: Using LLMs to diagnose medical issues based on personal health records. Using LLMs to diagnose medical issues based on personal health records.
        - E4: Ethical considerations apply to all of these use cases, but two options have a greater potential to cause harm.
        
        Utilizing LLMs to make decisions on behalf of people exposes them to a wide range of pitfalls. Careful attention is needed to prevent biases encoded into the models from leading to harmful decisions.
        
        Employing LLMs for diagnosing medical issues carries the risk of private data leakage, which could potentially be incorporated into future versions of the model.
    - Q5: What is the purpose of "fine-tuning" in the context of LLMs?
        - A5: It trains LLMs further on specific datasets to specialize them for particular tasks.
        - E5: Fine-tuning involves training LLMs on specific datasets to make them experts in particular domains or adapt to specific styles of text generation. It allows LLMs to specialize and improve their performance in specific tasks.

3. [ChatGPT Prompts, Completions, & Tokens](https://platform.qa.com/course/chatgpt-prompts-completions-tokens-4132/chat-gpt-prompts-completions-tokens/)

a. ChatGPT Prompts, Completions, & Tokens
- ChatGPT prompt: A sentence or phrase that is presented to the ChatGPT language model to generate a response. 
- Prompt: An input to the model. The question asked to ChatGPT. 
- ChatGPT completion: Response generated by the ChatGPT language model when presented with a prompt. 
- ChatGPT token: A unit of text that the ChatGPT language model uses to understand and generate language.

b. Knowledge Check
- Q1: Which of the following best describes tokens when using ChatGPT?
    - A1: The representation of text characters
    - E1: When using ChatGPT, the text of the prompt and completion are represented by tokens. Each chat session has a limited number of combine tokens.

- Q2: Which of the following best describes completion when using ChatGPT?
    - A2: The response from the model
    - E2: A completion is the response from the model. It is the answer given by ChatGPT.

- Q3: Which of the following best describes a prompt when using ChatGPT?
    - A3: The input to the model
    - E3: A prompt is an input to the model. It is the question asked to ChatGPT.

4. [ChatGPT Prompt Engineering, Role Prompts, and Chain Prompting](https://platform.qa.com/course/chatgpt-prompt-engineering-role-prompts-chain-prompting-4168/chatgpt-prompt-engineering-role-prompts-and-chain-prompting/)

a. ChatGPT Prompt Engineering, Role Prompts, and Chain Prompting
- Prompt engineering: The process of refining a given prompt to obtain the best possible answer that fits your scenario.
- Process of refinement, continuously pushing to find the best possible answer.
- Role Prompting: Asking for the AI to assume a given role, also referred to as an identity, before performing a given task. In this case, act as a copywriter.
- Chain Prompting: Asking for the AI to assume a given role, also referred to as an identity, before performing a given task. In this case, act as a copywriter.

b. Knowledge Check
- Q1: One of the riles stated for Prompt Engineering is to (force ChatGPT to be more concise.)
    - E1: When needed, it is best to force ChatGPT to be more concise. This allows for better and more specific answers.
- Q2: Which of the following best describes Prompt Engineering?
    - A2: The process of refining a given prompt.
    - E2: Prompt Engineering is the process of refining a given prompt to obtain the best possible answer that fits your scenario.
- Q3: Giving ChatGPT an identity is referred to as (Role Prompting).
    - E3: Role Prompting is asking ChatGPT to assume an identity when asking a question.

5. [Introduction to the OpenAI Chat Completions API](https://platform.qa.com/lab/introduction-to-the-openai-chat-completions-api/) 
- This lab introduces the OpenAI chat completion API and demonstrates how to use it to programmatically generate conversational responses. 
- Tools: OpenAI Python client library (chat completion API), Jupyter Notebook
- Hands-on Lab: [Introduction to the OpenAI Chat Completions API](assets/intro_openai_chat_completions_api_lab.ipynb)

6. [Introduction to GitHub CoPilot](https://platform.qa.com/course/introduction-github-copilot-4684/introduction-to-github-copilot/)

Knowledge Check:
- Q1: What are GitHub Copilot's limitations?
    - A1: It can suggest outdated or irrelevant code.
    - A1: It can be less capable for certain programming languages such as Rust and Haskell.
    - E1: GitHub Copilot may exhibit reduced capabilities for specific programming languages. It undergoes training on extensive datasets derived from publicly available projects. Programming languages with fewer real-world instances may receive poor recommendations. Copilot may frequently propose outdated code suggestions, primarily because of infrequent updates to the underlying large language model.
- Q2: How does GitHub Copilot adapt its recommendations?
    - A2: By using related files for context.
    - A2: By using the current file for context.
    - E2: Copilot uses both current and related files to inform recommendations.
- Q3: What is the primary purpose of GitHub Copilot?
    - A3: To generate repetitive and boilerplate code.
    - E3: GitHub Copilot's primary purpose is to assist developers by generating boilerplate code for software projects, making the coding process more efficient.

7. [Amazon CodeWhisperer: Generating Code with AI](https://platform.qa.com/course/amazon-codewhisperer-generating-code-ai-4679/introduction-1725534386341/) 

a. Knowledge Check:
- Q1: What can Amazon CodeWhisperer generate for you?
    - A1: Code snippets, Unit tests, Full functions
    - E1: Not only is Amazon CodeWhisperer helpful in terms of generating small code snippets, it’s also helpful in creating full functions and writing unit tests. You can use comments in your code to describe the function, test, or code snippet you’d like to write, and then wait for CodeWhisperer to complete the code for you.

- Q2: Which of the following AWS tool is Amazon CodeWhisperer integrated with automatically?
    - A2: AWS Cloud9
    - E2: To use CodeWhisperer, you download the AWS Toolkit extension for your IDE and integrate CodeWhisperer. Some IDEs such as AWS Cloud9 already have CodeWhisperer built-in directly to the service.
- Q3: Which of the following best describes the security scan feature of Amazon CodeWhisperer?
    - A3: It can detect common security issues before you commit your code, such as AWS Credentials issues and common OWASP security issues. 
    - E3: With security scans, you can scan your Python, Java, and JavaScript code for hard-to-find vulnerabilities such as those in the top 10 Open Worldwide Application Security Project (OWASP) or those that don't meet crypto library best practices and other similar security best practices.

8.[Understanding the Azure Open AI Service](https://platform.qa.com/course/understanding-azure-openai-service-4483/introduction-1725534384773/)

9. [Introduction to AI Copilot in Microsoft Power Apps](https://platform.qa.com/course/introduction-ai-copilot-microsoft-power-apps-4429/) 

a. Knowledge Check:
- Q1: You create a Power App using a single statement of up to 200 characters, but you are not happy with the initial data structure. How can you use Copilot AI to get the database table how you want it?
    - A1: Upload an Excel file with sample data.
    - A1: Use Copilot AI within the table creation screen to add, delete, or modify columns to customize the initial table.
    - E1: There is Copilot AI functionality within the table definition screen, allowing you to use natural language to alter the table’s structure. Alternatively, you can upload an Excel file of sample data that Copilot AI will interpret to create a table with appropriate data types. The quality of the sample data, that is, how clean and representative of what you’re trying to achieve it is, will determine how successful this approach is.
- Q2: What are the chracteristics of Power Apps that allow Copilot AI to easily augment app development?
    - A2: Power Apps’ relatively simple data-driven application structure.
    - A2: Power Apps low-code, no-code development paradigm.
    - E2: Power Apps employ a low-code, no-code data-driven development methodology where the apps are created from a series of pre-defined templates that are customized according to the underlying data they are interacting with. Copilot AI is used at the front end of the development process to design the data structure from which the app’s structure and functionality is derived.
- Q3: Which of the follwing best describes how AI is integrated into Power Apps?
    - A3: Copilot integrates natural language processing into Power Apps, enabling users to query organizational data.
    - A3: Copilot AI uses natural language processing to create simple data-driven applications.
    - E3: Copilot AI can be used to create simple Power Apps and be used within a Power App to query the app’s data. Copilot uses AI to interpret natural language, enabling a user to specify the underlying data structure using plain text. Power App Studio has a Copilot control that, when dropped onto a form and wired up to the app’s data source, will allow users to query the backing database with natural language.

10. [Introduction to AI Copilot in Microsoft Power Virtual Agents](https://platform.qa.com/course/introduction-ai-copilot-microsoft-power-virtual-agents-4582/)

a. Knowledge Check:
- Q1: How many subsites can CoPilot search under the generative answers URL?
    - A1: N/A
    - E1: While the URL for generative content can only be two sublevels deep, the bot can delve into any subsites within there as long as they are all under the same top level domain.

- Q2: What is the name of the setting to manage boosted conversations accuracy?
    - A2: Bot Content Moderation
    - E2: The setting to manage boosted conversations accuracy is "Bot Content Moderation".

- Q3: Which of the following are requirements for generative answers?
    A3/ E3: When utilizing generative answers, the 3 main requirements are:
        - Must be a Bing indexed website
        - Must not include sites with public forums
        - Must be at most 2 sublevels deep into a site

11. [Introduction to Google Generative AI Studio](https://platform.qa.com/course/introduction-google-generative-ai-studio-4427/)

a. Knowledge Check:
- Q1: When tuning a model in Generative AI Studio, what is the minimum number of examples you must include in your JSONL file?
    - A1: 10
    - E1: Your dataset must include a minimum of 10 examples, but we recommend at least 100 examples for good results. Generally speaking, the more examples you give, the better the results.

- Q2: How do you increase the randomness of the text responses in Generative AI Studio?
    - A2: Increase the temperature value
    - E2: Temperature controls the degree of randomness in token selection. Lower temperatures are good for prompts that require a more deterministic and less open-ended or creative response, while higher temperatures can lead to more diverse or creative results.

- Q3: When designing a new prompt in Generative AI Studio, what is the "context" field used for?
    - A3: Providing useful background information on your task
    - E3: Use context in a chat prompt to customize the behavior of the chat model. For example, you can use context to tell a model how to respond or give the model reference information to use when generating a response.