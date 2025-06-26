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
- Knowledge Check:
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

c. ChatGPT Prompts, Completions, & Tokens

d. ChatGPT Prompt Engineering, Role Prompts, and Chain Prompting

e. Introduction to the OpenAI Chat Completions API 

f. Introduction to GitHub CoPilot

g. Amazon CodeWhisperer: Generating Code with AI 

h. Understanding the Azure Open AI Service

i. Introduction to AI Copilot in Microsoft Power Apps 

j. Introduction to AI Copilot in Microsoft Power Virtual Agents

k. Introduction to Google Generative AI Studio