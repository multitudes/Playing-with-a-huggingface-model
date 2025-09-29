# Workshop: Play with a Hugging Face model (Part 1)

<a target="_blank" href="https://colab.research.google.com/drive/1AFSZrjC5aMhtxnbYWh3RYOSjdxd1iPjZ?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Meet Qwen3-0.6B, our new chatty friend. 

## The challenge
In this project, we will instantiate an instance of this model and see how the `vocab.txt` is set up. We will then create our own BPE tokenizer.
We have a set of prompts in our `function_calling_tests.json` file in the `exercise_input` folder and a set of tools defined in the `functions_definition.json` file, and our model needs to reply to each prompt with the correct tool to use. The output of the model must be in JSON format. This is the challenge.

Click on the "Run in Colab" button to see the notebook in action. Choose the T4 GPU to speed up the response generation.  The program will output the results to a JSON file in the `output` folder on Colab.

The notebook is included in this GitHub repository too.

## Launching Colab
When Colab is launched the first thing I do is clone the github repo to get the input files and merges.txt files to use for the exercise. This is a bit of a hack. If I were to put the files on my Google Drive then they would not be public and Colab doesnt allow me to save files on the notebook.

## Instantiating the hugginface model

We do not need to manually download the model or tokenizer files. The process is fully automated:

PyTorch is the deep learning framework used for computation and model inference.
Hugging Face Transformers (transformers library) handles model and tokenizer loading.
huggingface_hub (hf_hub_download) is responsible for downloading files (like vocab.json, model weights, etc.) from the Hugging Face Hub.
How it works:
I use the class `Small_LLM` in the notebook which will automatically download the required model and tokenizer files from the Hugging Face Hub if they are not already cached locally.
The line from huggingface_hub import hf_hub_download imports the function that fetches files from the Hub. This is used in get_path_to_vocabulary_json() to ensure you have the correct vocabulary file.


More docs to come... about the code.

## Resources
https://huggingface.co/Qwen/Qwen3-0.6B  
If you need the merges.txt files:  
https://huggingface.co/Qwen/Qwen3-0.6B/tree/main  
