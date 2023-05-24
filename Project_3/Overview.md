# Project 3: In the Shoes Of...  
An application that allows users to visualise themselves in the shoes of their favorite athletes using AI generated imagery. They can upload a few photos of themselves, which will be used to finetune an AI model so it can accurately replicate their face and place it in fictional sports-related scenes, creating something completely unique and personalized.

## Research Questions
The following are the research questions I tried to answer with this project. The methods used, as well as the conclusions, can be found in the [research report](/Research_Report.md).
- **How can I use generative AI to increase fan engagement?**  
This project is probably the one that most directly adresses this question, considering it's meant to be used by fans directly. I want to make use of that opportunity to do some user research, investigating how I can best engage people, and create something they're excited to use.  
- **What different types of generative AI exist, and how can they be used in innovative new ways?**  
This project is definitely even more on the bleeding edge of AI development than the previous two, meaning there are no ready-to-use APIs or tools I can use. This means I'll have to do preliminary research to investigate how and if what I want to do is possible, and how to best achieve good results.  
- **What are the needs of TDE's various customers, and how can I fulfill those?**  
Contrary to the other two projects, this one wasn't started specifically to fulfill a need of one of TDE's clients. Starting with a concept will mean there's some interesting research to be done into what client could best benefit from what I create, and how it could best be pitched to them.  
- **Where does the passion of the sports fans that consume TDE's products lie, and how can I use AI to respond to those passions in a positive way?**  
Many people, including myself, are wary of AI as a technology. I want to use this project to investigate uses of AI that are positive and fun, and being able to offer something to sports fans directly is a great opportunity for that.  
- **What ethical considerations have to be taken into account when working with generative AI?**  
While people are supposed to make use of the tool voluntarily, which mitigates some of the ethical concerns, there is still a lot to be taken into account - misinformation or abuse are always a possibility, and data storage and privacy is still a concern. I want to make sure the tool is as safe as it can be, by examining how it could be abused and how I can prevent that.  

## Project Process
### Initial Research and First Steps
I set up a meeting with several client leads at TDE to discuss potential uses for a tool like the one I'm making. Initially, it was supposed to be a pitch for BN Media, a group operating many football fan sites, to create a fun tool for fans of a specific football club to generate images of themselves playing for their team. TDE, however, saw more potential in the project, and some of the client leads thought it would be a waste to not use it for something bigger. They offered some potential alternatives (like the football european cup) but in the end we decided to turn this project into a proof-of-concept, waiting for a better opportunity to present itself to actually offer it to a client.

This is the most complex project out of the three by far, so I needed to do some initial research to get situated and get my bearings. After getting a general idea of what would be required, I set up a Kanban board to plan out the rest of the project.

### Further Research
For this project, I would need to train a generative AI model to be able to reproduce specific faces, as well as other objects like sports jerseys. Given the complexity of the subject, I spent several weeks on researching ways of achieving this goal, the process and results of which can be found [here](AI_Finetuning_Research.md).

Based on this research, there were some other observations I made regarding the project. First of all, fine-tuning an AI model still requires a large amount of processing power, something which is unlikely to change any time soon, which means that a tool like this would most likely require some form of payment or risk becoming very expensive to operate for a large userbase. Another consequence of this processing power is that the training will take a few hours at least. This is fine, but it does mean I won't be able to offer an easy-to-use app that gives results within minutes.

Another consideration is that generative AI is still relatively unpredictable, and tends to generate a lot of strange or nonsensical results, which means that a set of images will need to be generated every time, allowing users to pick their favorites.  
I did do some seperate research into ways to ensure the results would be as good as possible, and there are a few options. The first is good prompt engineering, making use of positive and negative prompts to get reliable results. Another options is the addition of an art style; a more 'loose' artstyle can hide imperfections that would be obvious in more photorealistic results. Some of the same techniques of finetuning can also be used to teach a model new styles, which will come in handy.  
Lastly, the more complex the desired end result is, the more can go wrong. To help steer the results in the right direction, it can help to provide hand-picked 'seeds', which will affect the composition of the end result without locking down the details.

### Development
I had originally intended to create an application that would allow a user to upload pictures of themselves in order to finetune the AI model, with them being able to generate pictures using that model afterwards, but this proved challenging. 
Firstly, the training takes a lot longer than I anticipated, especially on a consumer grade PC. This means that either the application would need to keep running for over 24 hours without interruption, or I would need to set up an expansive and seperate backend to do the training, save the results, and somehow notify the user once it's done.
Also, the underlying code required to finetune models is very complex, and while I did get it working to a degree (the code can be found [here]()), the results weren't as good as I'd hoped.
Eventually I decided to forego this part of the app entirely: due to the feature's complexity, getting it working and stable would take much more time than I had available. Instead, I used this project to investigate and showcase the potential of AI fine-tuning.

The image generation part of the application was a lot more manageable to implement, considering it was fairly similar to the first project. I also did a lot of experimenting with the prompt used to generate the image, to try and get the most consistent results, comparisons of which can be seen [here]().

## Results and Reflection
While it's a shame that I couldn't implement the fine-tuning in the application, I'm still quite happy with the end result. I think the project was a great platform for (user) research, and a great culmination of everything I'd learned about AI in the internship.  

In the end, the original idea proved to be a bit too ambitious for a few reasons. There was the technical complexity which I discussed earlier, but I also ran into limitations when it came to the AI models themselves. Unfortunately, text-to-image models aren't yet able to consistently generate complex images like an action shot from a football match, so the results aren't quite at a level of quality where I'd be willing to release the tool to the greater public. Pushing up to and investigating these limits was a great way to get a good idea of what the technology is capable of, and I think the current iteration of the application works very well as a showcase of what generative AI is currently capable of.

Planning-wise, I think I was able to manage the project quite well. The Kanban board allowed me some flexibility, which came in very handy when it turned out the project's research phase was more complicated, and would thus take longer, than expected.

If I had more time to work on it, there are quite a few improvements I still have in mind. One of those is getting the finetuning to work fully, but I also think there are some gains to be had with the image generation aspect. There are still a few tricks and techniques for improving results that I didn't get to try, for example 'locking' the AI into a good composition using seeds, generating using an existing image, or further finetuning the model.

## Deliverables
[Research report on AI finetuning]()  
[Results and discussion of user testing]()   
[Ethics and privacy report]()  
[Repository for the application]()  
[Frontend design]()  
