# Introduction to building Generative AI Apps and Solutions
- [Prompts and Prompt Engineer](#prompts-and-prompt-engineer)
- [Generative AI Features and Solutions](#generative-ai-features-and-solutions)
- [Prompt template](#prompt-template)
- [Generative AI Components](#generative-ai-components)
- [Building AI Agents](#building-ai-agents)
- [Function Calling](#function-calling)

## Prompts and Prompt Engineer
Prompts are input statements or questions that are provided to a model to generate a desired output or response.

![image](https://github.com/user-attachments/assets/50522311-fcbe-473d-9ffa-7012c7a68f36)

Prompts and Prompt engineer helps bridge the model and the application layers:
- Without well-engineered prompts, generative models can provide poor output, resulting in your application not working the way you envisioned it.
- Code in the application layer often pre-processes or structures user input into effective prompts for the model.

## Generative AI Features and Solutions
- Generative AI refers to models that can create new content, such as text, images, or music, rather than just analyzing existing data.
- It opens up vast possibilities for innovative applications across various industries, enabling the generation of contextually relevant content tailored to user needs.
- Benefits: Generative AI can enhance creativity, automate content creation, and improve user engagement by providing personalized experiences.
- How It Works: The lesson likely covers the underlying mechanisms of generative models, such as neural networks and training processes that allow these models to learn from data and generate new outputs.
- Real-World Examples: There may be discussions on how companies are leveraging generative AI to solve problems, improve efficiency, and create new products or services.

## Prompt template
- Establishes how users interact with the systems, how the format or structure of the users' inputs should be.
- Provides a user-frinendly interface for users to interact with the applications
- Sets expectations of what the LLM models can and can't do
- Produces effective outputs as they are heavily dependent on the specificity and clarity of users' inputs.
- Easy for developers to maintain and modify with large AI applications
- Reduces the likelihood of errors and misunderstanding due to users' poor input -> increase accuracy and precision.
- Example: [GenAIFeatureDesignPromptTemplate](./GenAIFeatureDesignPromptTemplate.ipynb)

## Generative AI Components
- LLM models: The core of Generative AI Applications, where users input are processed and outputs are generated
- Application Logic: acts as controller that processes users input before sending them to the models. Once the models generate the output, the application logics also process the outputs before displaying it to users
- User Interface: Through which users interact with the model. This is where users provide their prompts and inputs for the models to process.
- Database: store users' information and AI responses. They can also be vector databases, which can be used for RAG (Retrieval Augmented Generative)
- API: Allows the applications to connect to external services and platforms. This is also the means for the appliation to communicate with other AI models.
- Example: [GenAIFeatureSocialMediaPost](./GenAIFeatureSocialMediaPost.ipynb)

## Building AI Agents
- Perform automation tasks, mimicking human's decision making
- Allow the agents to interact with outside resources like databases and the Internet to complete its tasks
- Can be autonomouse or semi-autonomous. Can perceive and react to environments, making decision without or with little humans' interactions.

### ReAct Prompting for Agents
A popular prompting method called ReAct can be used to create LLM-based agents. REACT prompt techniques use LLMs to generate both reasoning traces and task-specific actions.

- The reasoning aspect involves the AI agent thinking through a problem, breaking it down into smaller, manageable parts, and forming a plan or series of steps to solve it.
- The action component allows the agent to make decisions about gathering additional information relevant to the task.
- The observation step often involves delivering a final response about a task or recording an event. These observations can be used for further reasoning. REACT-enabled agents actively seek out new information, update their understanding, and refine their reasoning based on observations.

A REACT prompt for a wellness agent might be: "Your goal is to improve the wellness of the user by interleaving thought, action, and observation."

- Example: [WellnessAgent](./WellnessAgent.ipynb)

## Function Calling
- Provides a structured method for directing an AI's generative capabilities, allowing it to produce specific and actionable outputs.
- Helps standardize responses, ensuring they follow a consistent format that can be easily interpreted.
- Allows models to interact with external APIs or databases, enabling real-time data retrieval.
- Essential for improving the practicality of LLM applications by ensuring consistent response formats, enabling integration with external data sources, and allowing the AI to perform structured tasks relevant to user needs.
- Example: [FunctionCallingDemo](./FunctionCallingDemo.ipynb)

### Exercise - Build a Project Management Assistant
In this exercise, you'll build a project management assistant that uses the OpenAI API function calling. You'll use reading and writing to a CSV file to simulate reading and writing from a database or project management tool API.

Solution: [BuildProjectManagementAssistant](BuildProjectManagementAssistant.ipynb)
