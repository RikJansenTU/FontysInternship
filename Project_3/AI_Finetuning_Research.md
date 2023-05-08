# Finetuning a Generative AI Model to Suit Your Needs
The release of OpenAI's DALL-E generative AI model for generating images based on user-submitted prompts was probably the event that launched generative AI into the public consciousness. Any user could suddenly generate artwork in seconds, making AI tangible and accessible even to those without a technical background.
Ever since, these so-called text-to-image AI models have been advancing rapidly. [Midjourney]() was released to the public in July 2022, rapidly becoming extremely popular to it's ease of use and high quality output. In the same month, [DALL-E 2]() entered its own beta, boasting a range of improvements over its predecessor.  
The model I am most interested in for my purposes, however, is [Stability AI's Stable Diffusion](). This model is relatively lightweight, meaning it can run on consumer hardware, and most importantly it's completely open-source. The latter has led to a flurry of tools and methods to customize the model to suit your exact needs - something I can make good use of for my project. This process is called fine-tuning; making adjustments to an existing AI model so it learns to generate specific content, for example being able to replicate specific faces.

I have created the following requirements for the application I'm building:  
- **Accurate:** especially when it comes to their own faces, people will easily be able to spot small imperfections, which means the application will need to be quite good at replicating them.
- **Multiple parameters:** aside from faces, the model will likely need to be fine-tuned on other things, like specific football kits, which means the chosen method will need to be able to accommodate multiple adjustments.
- **Small:** the application is supposed to be used by a large group of users, resulting in a lot of fine-tuned models that will have to be stored, so the smaller the file the better.
- **Fast:** the longer users have to wait to get their result the less attractive using the application will be. Faster models will also require less processing power, lowering the operating costs.

The goal of this research is to investigate the different methods of fine-tuning an AI model, finding the one that best suits my needs, and learning how to implement it. 

### Research Methods
Mostly literature research and available product analysis where possible  
Challenge, no real documentation or good tutorials available yet

### Finetuning Methods
First, a quick word on the text-to-image model I've elected to use: Stable Diffusion 1.5. The choice for this model is an easy one, it being the only high quality fully open-source model available, which means many fine-tuning methods were either developed for Stable Diffusion, or quickly adapted to it. For this reason, it has also become the centerpiece of the text-to-image community.  
I am using the 1.5 model, even though the newer 2.0 and 2.1 are publicly available - the reason for this is that version 2 was trained on a different image set, and many users actually report worse and less reliable results when using it.

There are four main methods of finetuning a text-to-image model: Dreambooth, textual inversion, LoRA, and hypernetworks. Each work in slightly different ways, and have different advantages and disadvantages, all of which I will summarize below.

**Dreambooth**
Dreambooth is a fine-tuning method for diffusion models published by Google in 2022, which allows you to inject a custom subject into the model based on a few pictures and a matching identifier. As a result, the model can generate highly accurate reproductions of the subjects in a variety of new situations. The model gets retrained completely, requiring a large amount of processing power and resulting in a very large file (2-5 GB) for each fine-tuning.
  Dreambooth: good results but very large  
  
**Textual Inversion**

**LoRA**



**Hypernetworks**
Hypernetworks is a fine-tuning method developed by [NovelAI](), which inserts small neural networks into the cross-attention layer of the original model. They are lightweight, small in size, and relatively easy to train. However, it is difficult to train a hypernetwork on multiple subjects, and users report worse results compared to LoRA or embeddings, with little to no gain in size or performance.

Large processing power requirements  -> expensive, probably won't work for a free tool  
Results are unpredictable  
  Stylistic changes can help hide imperfections  
The bigger the image the more can go wrong
  Image to image, using a few base images to make sure composition etc are solid
  Composition: can pick a few good seeds and reuse those  


  https://civitai.com/  
 VAE for improvements
  
 Realistic Vision V2
 
 First Finetune on eg PSV shirt, then use user photos to further finetune

### Conclusion and Implementation

Implementation: attempted, but very difficult to do programmatically -> use automatic1111  
Do inference in software, more proof of concept


### Glossary of Terms
**Diffusion Model**  
**Fine-Tuning**  
**Generative AI**  
**Latent Model**  
**Text-to-Image Model**  

### Tutorials
https://www.youtube.com/watch?v=usgqmQ0Mq7g  
https://www.youtube.com/watch?v=2ityl_dNRNw  
https://www.youtube.com/watch?v=dl7CSdzvl44  
https://www.youtube.com/watch?v=dfMLrytpfAU  
https://www.youtube.com/watch?v=XBn3K1L_TAI&t=1s  
https://andrewongai.gumroad.com/l/dreambooth_tutorial  
https://stable-diffusion-art.com/dreambooth/  
https://stable-diffusion-art.com/how-to-come-up-with-good-prompts-for-ai-image-generation/#Some_good_keywords_for_you  
https://stable-diffusion-art.com/automatic1111/  
https://stable-diffusion-art.com/prompt-guide/  
https://huggingface.co/docs/diffusers/quicktour
https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/sd_textual_inversion_training.ipynb
https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/stable_conceptualizer_inference.ipynb
https://www.youtube.com/watch?v=dVjMiJsuR5o
https://huggingface.co/docs/diffusers/optimization/xformers
https://huggingface.co/docs/diffusers/optimization/fp16#memory-and-speed

### Sources
https://dreambooth.github.io/  
https://github.com/XavierXiao/Dreambooth-Stable-Diffusion  
https://arxiv.org/abs/2208.12242  
https://textual-inversion.github.io/  
https://arxiv.org/abs/2106.09685  
https://lexica.art/
https://artificialintelligenceact.eu/
https://huggingface.co/blog/ethics-diffusers
https://www.pnas.org/doi/10.1073/pnas.1611835114
https://github.com/facebookresearch/xformers  
https://www.semianalysis.com/p/google-we-have-no-moat-and-neither
https://arxiv.org/abs/1909.04499

### Huggingface stuff
https://huggingface.co/docs/diffusers/main/en/api/pipelines/stable_diffusion/latent_upscale
https://huggingface.co/docs/diffusers/training/text_inversion
https://huggingface.co/docs/diffusers/v0.16.0/en/api/pipelines/stable_diffusion/text2img#diffusers.StableDiffusionPipeline
https://github.com/huggingface/diffusers/blob/main/examples/textual_inversion/textual_inversion.py

### Styles
Marc Allante
Valorant
Midjourney
Arcane
