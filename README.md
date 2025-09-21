# Workshop: Play with a Hugging Face model (Part 1)

<a target="_blank" href="https://colab.research.google.com/drive/1AFSZrjC5aMhtxnbYWh3RYOSjdxd1iPjZ?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Meet Qwen3-0.6B, our new chatty friend. 

In this project, we will instantiate an instance of this model and see how the vocab.txt is set up. We will also create our own BPE tokenizer.

We have a set of prompts and a set of tools, and our model needs to reply with the correct tool to the prompt in JSON format. This is the challenge.

Click on the "Run in Colab" button to see the notebook in action. Choose the T4 GPU to speed up the response generation. 

The program will output the results to a JSON file in an output folder (look on the left in files and you will find it).


## Resources
https://huggingface.co/Qwen/Qwen3-0.6B  
If you need more files:
https://huggingface.co/Qwen/Qwen3-0.6B/tree/main  