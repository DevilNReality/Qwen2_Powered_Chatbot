# Qwen2_Powered_Chatbot

## **🧠 Instruction-Tuned Chatbot with Qwen2**
This project demonstrates how to build a lightweight conversational AI assistant using Hugging Face Transformers and Gradio. It’s designed to be modular, beginner-friendly, and optionally fine-tunable using instruction-style data.

## **📌 Project Overview**
The chatbot uses the Qwen/Qwen2-0.5B-Instruct model—a compact, instruction-tuned language model developed by Alibaba. It’s optimized for prompt-following and conversational tasks, making it ideal for building assistants that respond clearly and naturally.

### **The project includes:**
1. *A simple Gradio-based user interface*
2. *Optional conversation history*
3. *Modular response generation logic*
4. *Instruction tuning support using CSV-formatted data*
5. *A clean README for reproducibility and sharing*

## **🚀 Setup**
### **To run the chatbot locally:**

**1. Install Required Libraries**

This project uses four key Python libraries:

* **Transformers** – *for loading and interacting with the Qwen2 model*
* **Datasets** – *for handling instruction tuning data*
* **Gradio** – *for building the web-based chatbot interface*
* **Pandas** – *for preparing and saving the training dataset*

These can be installed using pip. Once installed, your environment is ready to run the chatbot or prepare it for fine-tuning.

**2. Load the Pretrained Model**

The chatbot uses Qwen/Qwen2-0.5B-Instruct, a small but powerful instruction-tuned language model. It’s downloaded automatically from Hugging Face when the script runs, so no manual setup is required.

The model is loaded along with its tokenizer, which breaks down user input into tokens the model understands. The tokenizer is also configured to pad shorter inputs and truncate longer ones, ensuring consistent input size during training and inference.

**3. Initialize the Chatbot Persona**

Before the chatbot starts interacting, it’s given a system prompt that defines its personality. In this case, the assistant is set to be helpful, friendly, and conversational. This prompt helps guide the model’s tone and behavior throughout the session.

An initial greeting message is also added to the chat history so users are welcomed when the interface launches.

**4. Launch the Gradio Interface**

Gradio is used to create a simple, interactive web interface. It displays the conversation history and allows users to send messages to the chatbot. The backend logic handles user input, generates responses using the model, and updates the chat history in real time.

Once launched, the chatbot is ready to use—no additional configuration is needed.

## **🧠 Usage**
Once launched, the chatbot accepts user input and responds conversationally. It maintains optional history for multi-turn interactions and uses sampling techniques to generate diverse, natural replies.

### **You can:**
1. *Ask questions*
2. *Request translations*
3. *Get summaries or lists*
4. *Extend the assistant’s behavior with custom instructions*

## **📁 Instruction Tuning (Optional)**
### **If you want to fine-tune the model:**
1. *Prepare a CSV file with input and output columns*
2. *Format each example using Qwen2’s prompt style (<|user|> and <|assistant|>)*
3. *Tokenize and preprocess the dataset*
4. *Use Hugging Face’s Trainer to fine-tune the model on your custom data*

This step is optional and can be skipped if you're using the pretrained model as-is.

## **🙌 Credits**
Built by **Karthikeyan V** as part of a hands-on LLM deployment and instruction tuning exercise. The project is designed to be beginner-friendly, reproducible, and adaptable for real-world applications.
