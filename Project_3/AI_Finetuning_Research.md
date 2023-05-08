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
This is a field of technology that is both very new and rapidly advancing, which made researching a challenge; while many research papers have been released over the past couple of years, there is a lack of meta-analysis or comprehensive tutorials on implementations. Most of my research was literature study, first gathering information on the different fine-tuning methods abailable and later investigating how they worked. I tried to analyse their differences, finally setting up prototypes and judging the results.

### Fine-tuning Methods
First, a quick word on the text-to-image model I've elected to use: Stable Diffusion 1.5. The choice for this model is an easy one, it being the only high quality fully open-source model available, which means many fine-tuning methods were either developed for Stable Diffusion, or quickly adapted to it. For this reason, it has also become the centerpiece of the text-to-image community.  
I am using the 1.5 model, even though the newer 2.0 and 2.1 are publicly available - the reason for this is that version 2 was trained on a different image set, and many users actually report worse and less reliable results when using it.

There are four main methods of finetuning a text-to-image model: Dreambooth, textual inversion, LoRA, and hypernetworks. Each work in slightly different ways, and have different advantages and disadvantages, all of which I will summarize below.

**Dreambooth**  
Dreambooth is a fine-tuning method for diffusion models published by Google in 2022, which allows you to inject a custom subject into the model based on a few pictures and a matching identifier. As a result, the model can generate highly accurate reproductions of the subjects in a variety of new situations. The model gets retrained completely, resulting in a very large file (2-5 GB) for each adaptation.
  
**Textual Inversion**  
Textual inversion is a technique that also allows you to 'teach' new subjects to a diffusion model, but unlike Dreambooth the image generation model itself isn't changed. Instead, it affects the part of the AI that controls how a prompt gets used to generate an image, inserting a new keyword. Textual inversion basically allows you to add a new term to the AI's vocabulary. Because the image generation model isn't affected, the file resulting from the fine-tuning process is much smaller, usually around 100 KB.  
These files are called embeddings, and because of the way they work it's possible to add a variety of new subjects and even artstyles to the same embedding, allowing a great degree of customization. They produce relatively good results based on just a few pictures, but training does take a relatively long time.

**LoRA**  
LoRA stands for Low-Rank Adaptation, and modifies the cross-attention layer of the diffusion model, the part where the prompt is used to steer the image generation in the right direction. LoRA adds and adjusts some weights in this layer, modifying it to be able to generate a new subject or style without having to completely retrain the model. To optimize this process, LoRA reduces the model's weights matrix into multiple lower-rank matrixes, resulting in relatively small file-sizes of around 100-200 MB, and a fast training time.  

**Hypernetworks**  
Hypernetworks is a fine-tuning method developed by [NovelAI](), which inserts small neural networks into the cross-attention layer of the original model. They are lightweight, small in size, and relatively easy to train. However, it is difficult to train a hypernetwork on multiple subjects, and users report worse results compared to LoRA or embeddings, with little to no gain in size or performance.

### Conclusion and Implementation
Objective comparison between the results different fine-tuning methods is difficult; there hasn't been much research performed into their differences, and because their results are images it's hard to make meaningful distinctions. Because of the relatively long training times, especially on my own PC, it's also difficult to set up prototypes to do testing myself.

There are some other considerations to take into account, however. While Dreambooth seems to be able to produce the best all-round results, its large file sizes make it a bad fit for my application. Having to store a 2 GB file for every user would be highly impractical.  
The concensus about hypernetworks seems to be that they produce universally worse results than the other methods, which means they can be removed from consideration.  
That leaves textual inversion and LoRAs, the differences between which are much harder to quantify. Some report better general results when using the latter, whereas the former is sometimes considered to be better at reproducing people. Embeddings can easily be combined, for example allowing for the addition of both a specific sports jersey and a person's face to a single model. LoRAs are quicker to train, which is a great advantage, but the process will still take a few hours at least.

Seeing as textual inversion is a good fit for my purposes, I decided to try to prototype this method first. Implementation proved very difficult however; the subject matter is very advanced, and due to how new the technology is there are no tutorials on how to program the training process. I tried to implement as much as I could (the results of which can be found in the 'training' folder in the [code repository]()), but eventually realised that getting it to work would require more time than I had for this project.
Instead, I made use of external tools to train my embeddings so I could experiment with the best options. This did unfortunately mean I would't be able to implement training functionality directly into my own application, turning it from a feature-complete tool into a proof-of-concept. I do believe this is still very valuable as a way of exploring this category of generative AI, however.

Results of textual inversion  
Results of LoRA

#### Sources
- Dreambooth abtract and showcase  
https://dreambooth.github.io/  
- Dreambooth paper  
https://arxiv.org/abs/2208.12242  
- Dreambooth implementation for Stable Diffusion  
https://github.com/XavierXiao/Dreambooth-Stable-Diffusion  
- Textual inversion abstract and showcase  
https://textual-inversion.github.io/  
- Textual inversion paper  
https://arxiv.org/abs/2208.01618  
- LoRA paper  
https://arxiv.org/abs/2106.09685  
- Paper on overcoming catastrophic forgetting in machine learning algorithms  
https://www.pnas.org/doi/10.1073/pnas.1611835114  
- Repository for xFormers, optimizations for model training  
https://github.com/facebookresearch/xformers  
- Paper on countering language drift  
https://arxiv.org/abs/1909.04499   

https://www.semianalysis.com/p/google-we-have-no-moat-and-neither  
https://lexica.art/  
https://artificialintelligenceact.eu/  
https://huggingface.co/blog/ethics-diffusers  

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

### Huggingface stuff
https://huggingface.co/docs/diffusers/main/en/api/pipelines/stable_diffusion/latent_upscale
https://huggingface.co/docs/diffusers/training/text_inversion
https://huggingface.co/docs/diffusers/v0.16.0/en/api/pipelines/stable_diffusion/text2img#diffusers.StableDiffusionPipeline
https://github.com/huggingface/diffusers/blob/main/examples/textual_inversion/textual_inversion.py


### Styles
https://civitai.com/   
Marc Allante
Valorant
Midjourney
Arcane
