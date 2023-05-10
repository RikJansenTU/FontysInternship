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

## Deliverables
Deliverable: Research report on AI finetuning  
Deliverable: short examination of potential clients  
Deliverable: results of user testing   
Deliverable:  ethics and privacy report  

**Other Deliverables**  
Code  
Frontend design  

## Reflection & Future Steps

 VAE for improvements
  
 Realistic Vision V2
