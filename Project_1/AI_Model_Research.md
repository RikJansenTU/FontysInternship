# Research: AI Transcription and Summarization

## Transcription

AI-based speech recognition might seem relatively mundane compared to some of the things we see AI do these days, but it's still very much an open problem. A top-tier AI model will still get 1 in 20 English words wrong, and other languages are often worse. Dutch, which is an important language for my tool, can be recognised quite well, but the best models still have a word error rate of around 7%. 

Considering I still need to summarize the result of my transcription, these errors can be critical; when a user can see the full text it can be easy to infer the meaning of an incorrect word by context, but once that text gets summarized it might fundementally change the context and end result.

Accuracy isn't the only important factor however: speed is also of the essence. The larger a model, the more accurate it generally is, but the longer it will take to transcribe a text. Since my application is meant to save time, I can't ask users to wait hours to process a 20-minute podcast.

Since every AI model has different implementation requirements, it wasn't feasible to set up a prototype of every available speech recognition model. Instead I looked at available benchmarks, and based on those decided to go with OpenAI's Whisper, which outperforms most other speech recognition models available, as well as being open-source.

![Whisper Test Results](https://user-images.githubusercontent.com/9715331/227275260-4c2383b9-2eb2-4dbc-9715-469d377e0523.png)

Once I landed on Whisper, I could set up a functioning prototype and start testing. There has been a range of Whisper models released, with the smaller ones taking less time to process audio, but becoming more inaccurate. I wanted to strike the right balance between accuracy and speed, so using a recording of Martin Luther King's 'I have a dream' speech I tested out every Whisper model available.

Whisper has English-specific models available, that outperform their generic counterparts, but can't be used for other languages - these are the models with the '.en' suffix.

I tested once on a Macbook, using a CPU, and once on a PC using a GPU, to see the difference in speed. The audio file I used was 16 minutes and 27 seconds long. Below are my results.



As you can see, there is a significant jump in speed from the small to the medium model. The accuracy doesn't seem to change much between the models, but the 1% difference is more impactful than you might think. The summarizations that resulted from the 'base' transcriptions were much less coherent than those resulting from the 'small' transcriptions.

In the end, I opted to use the small models, using small.en if the English language is specified. While it does take slightly longer to transcript, it still has an acceptable speed, and the small increase in accuracy compared to the base model was significant enough to justify the longer time taken.


## Summarization

AI summarization is less of a challenge than transcription, and there are a lot of great models to choose from. It's a bit harder to objectively rate a summary, considering there is no 'right' answer, so I simply set up a prototype to try out a few summarization models and judged their quality myself. I used the Whsiper-generated transcription of a Dutch podcast as my original text, because I wanted to find a summarization model that could handle the kind of grammatical oddities that can result from imperfect transcriptions.
I ended up picking Facebook's Bart-large-CNN, a model fine-tuned on CNN articles and their summaries, which seemed to generate the most coherent summaries.

### Sources

https://cdn.openai.com/papers/whisper.pdf
