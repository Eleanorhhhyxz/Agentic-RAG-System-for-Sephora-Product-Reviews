# Agentic RAG System for Sephora Product Reviews
This repo stores the project code for an Agentic RAG System (with LoRA-finetuned sentiment analyzer) for the Sephora Product Reviews.   
The code contain an end-to-end pipeline of embedding/upserting raw data into a vector database, LoRA-based finetuning of a BERT-tiny model for sentiment analysis, and a multi-agent RAG workflow (via a graph-based pipeline) to answer user queries about Sephora product reviews. It also integrates the multi-agent graph workflow with a Flask-powered front-end web app, allowing users to input queries and view responses through a web interface.

# Repo Introduction  
- Agentic_RAG_System_Pipeline.ipynb: This is the main code for this project, which includes the Multi-agent RAG System, Graph Building, Front-End System Building and Testing Pipeline.  
  - The Front-End System is built through Flask and ngrok and included as part of this code, and it needs the graph workflow needs to be successfully compiled. It will output a link to a site built by ngrok. By clicking "Visit Site" in the linked page, it will show the front-end page, which allows user to input query and output response.
- Embedding_Upserting_Pipeline.ipynb: This code is the prerequisite for running the main code, which includes the embedding of the raw data and upserting of the vectore database. The link to Google Colab is on the top of the uploaded code.
- BERT_LoRA_Finetuning_Pipeline.ipynb: This is the finetuning code for the base model prajjwal1/bert-tiny with LoRA-based PEFT finetuning. The code will save the finetuned model in the required path. The finetuned model can be accessed in the shared Google folder for this project, with path GenAI_Stitching/finetuned_lora_model and link https://drive.google.com/drive/folders/1osoqazPHZDhjE5l1AUx7RCeciHWma6Bc?usp=drive_link.
- dockerfile: This dockerfile serves as the container for this project, and the docker image is built on a server from Northwestern MLDS.
- requirements.txt: This is the underlying required environment for running the main code, which is downloaded from Google Colab. To avoid environmental mismatch, it is advised to run the above codes via Google Colab.
- Outputs_and_Discussion.docx: This file contains the outputs and the discussion on outputs from the multi-agent system.
