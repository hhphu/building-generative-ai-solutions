# Introduction to building Generative AI Apps and Solutions
- [Prompts and Prompt Engineer](#prompts-and-prompt-engineer)
- [Generative AI Features and Solutions](#generative-ai-features-and-solutions)
- [Prompt template](#prompt-template)

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
