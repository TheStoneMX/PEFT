# PEFT
PEFT is a generic term that includes Low-Rank Adaptation (LoRA) and prompt tuning (which is NOT THE SAME as prompt engineering!). In most cases, when someone says PEFT, they typically mean LoRA. LoRA, at a very high level, allows the user to fine-tune their model using fewer compute resources (in some cases, a single GPU). After fine-tuning for a specific task, use case, or tenant with LoRA, the result is that the original LLM remains unchanged and a newly-trained “LoRA adapter” emerges. This LoRA adapter is much, much smaller than the original LLM - on the order of a single-digit % of the original LLM size (MBs vs GBs).

In the notebook Fine-Tune_generative_AI-Model, 
      1.- We perform Parameter Efficient Fine-Tuning (PEFT), 
      2.- evaluate the resulting model With ROUGE, and 
      3.- see that the benefits of PEFT outweigh the slightly lower performance metrics

On the notebook Fine-Tune FLAN-T5 with Reinforcement Learning (PPO) and PEFT, 
      1.- We will fine-tune a FLAN-T5 model to generate less toxic content with Meta AI's hate speech reward model. 
      2.- The reward model is a binary classifier that predicts either "not hate" or "hate" for the given text. 
      3.- We will use Proximal Policy Optimization (PPO) to fine-tune and reduce the model's toxicity.
