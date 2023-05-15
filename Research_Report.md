# Research Report
This report collects the research I've done across all my projects to answer the research questions, as well as my overall conclusions.

## How can I use generative AI to increase fan engagement?
This is the main research question I want to answer during my internship. Fan engagement is a broad concept in this context - it doesn't mean that everything I build will need to be used by sports fans directly, but it should serve them or improve their experience when interacting with TDE's products, which in turn will increase engagement.

### Methods
As this is my main research question, I didn't do any research into this subject directly. Instead, I formulated the other questions to cover different aspects of this one, coming to a general conclusion in the end.

### Conclusions

## What different types of generative AI exist, and how can they be used in innovative new ways?
Exploring the types of AI available, as well as their uses, will play an important part in achieving the internship's goals.

### Methods
**Available product analysis / community research:** Over the last years the number of freely available AI tools has exploded, so I'll have many I can use and build upon. I had to investigate if there were existing tools that suited my needs and how they could be implemented. Also, being aware of the available tools ensured I wasn't creating anything that already existed, and allowed me to identify areas where innovation was still possible.  
**Literature study:** If no ready-to-use tools were available, I had to figure out how to implement and apply generative AI models myself, which required research into how these models work.  
**Prototyping:** I set up a series of simple prototypes that I could use to test different models and compare them, as well as get to grips with the technology involved.

### Conclusions
AI tools are quickly becoming easier to use and implement for your own goals - for example, OpenAI released a Whisper API several weeks after I had finished project 1, making transcription significantly easier. For many areas, however, easy-to-use tools and well-implemented and documented APIs are still difficult to find, which can be both an advantage and a disadvantage.  
On the one hand, it made the engineering side of some of my projects significantly harder, but on the other hand it does mean that there is still a lot of space to innovate and create something completely new. I think the greatest potential for a company like TDE is in using and combining existing models to do something novel, keeping an eye on new developments and being one of the first companies to bring them to the greater public in an accessible way.  
I don't think trying to develop and train AI models from scratch is worth it for a company like TDE, considering the knowledge and costs required, especially seeing how many great models are available as open-source projects.

The Jupyter Notebooks with my prototypes for project 1 can be found [here](https://github.com/RikJansenTU/PodcastSummarizer).  
A more comprehensive research report on AI models used for transcription and summarization can be found [here](/Project_1/AI_Model_Research.md).  
A research report on fine-tuning a text-to-image AI model with custom subjects can be found [here]().  
Some samples from my experimentation with prompt building for the project can be found [here]().  

## What are the needs of TDE's various customers, and how can I fulfill those?
If I can anticipate these customers' needs, and find a way to use AI to meet them, TDE will be able to proactively offer solutions, potentially earning them new clients or additional assignments.

### Methods
**Brainstorm:**  I planned a brainstorm session with a few of my colleagues at TDE for every project, both so they could help come up with ideas for implementation and features, and so they could help theorise what the best use of the finished product was. Especially for project 3, which wasn't started with a specific client in mind, we spent some time discussing which client could best benefit from the tool, and how I could potentially play into their hand.  
**Interviews:** RacingNews365's office is located on the same floor as TDE, so they were easy to communicate with. The initial [requirements](/Project_1/Requirements.md) were formulated based on a meeting where they indicated their needs.  
I also discussed TDE's different clients with the client leads, to get a better idea of the type of customer the company tries to appeal to.
**Stakeholder analysis:**  The stakeholder I was most involved with was TDE themselves (specifically the client leads), with me creating AI tools that would showcase the technology's potential. I also tried to investigate TDE's clients, to figure out what their potential response to AI would be and how willing they would be to make use of it.

### Conclusions
I think AI currently best suited as a tool to speed up a process, for example by answering questions or writing a draft for a press statement. It isn't quite at a level where it can create something without human supervision, which means it's difficult to present a polished tool that delivers consistent results on its own.  
AI as a productivity tool has a lot of potential (as well as this being one of its most ethically justifiable uses, more on that below), but these types of tools are not really something TDE specializes in, and are difficult to present to clients.
Many of these client are also hesitant to make use of new technology and embrace unfamiliar strategies, which makes pitching something using AI difficult. All this means that creating tools for clients' use is rarely a worthwile effort; most are unlikely to be willing to pay for development.  
Instead, I think most potential for AI-powered tools is in internal use. TDE is in charge of quite a few advertising campaigns, and using AI for those is a great way of grabbing attention and getting people talking. There is also a lot of opportunity in using AI powered tools internally to improve productivity, for example by using ChatGPT-generated code or for generating first drafts of images. 
If TDE becomes an early adopter of the technology, they might be able to rival much larger companies even with their small team, and offer their clients more impressive results for smaller costs.

## Where does the passion of the sports fans that consume TDE's products lie, and how can I use AI to respond to those passions in a positive way?
The nice thing about a company that focuses on sports is that the end users tend to be very passionate about their engagement. This offers a unique opportunity to create something positive that these fans truly enjoy interacting with.  
### Methods
**Survey:** The third project was the only one that was aimed at sports fans directly, so I wanted to take the opportunity to do some user research, using surveys to gauge people's opinion on both that project directly and on AI in general.  
**Expert interviews:** The client leads at TDE have a lot more experience trying to appeal to sports fans, so I discussed my project with them, gathering their opinions on what would appeal and what wouldn't.

### Conclusions
Creating something that will be used by fans directly is difficult for a number of reasons. First, it means a tool needs to be much more polished, especially when it comes to something that is supposed to be a showcase for your company. This requires a proper frontend and good UX design, but most crucially you want the results to be good.
The latter is still very difficult, especially when it comes to text-to-image applications; while the current generation of generative AI models is incredibly impressive, consistency of results is still a challenge. Anatomy gets messed up, backgrounds become surreal, and faces get deformed; a bad result can reflect badly on TDE.
A tool for use by the public would either need to be very polished (which likely means limited) or users' expectations would need to be managed. Alternatively, using AI to create something the company normally wouldn't, handpicking the best results, and releasing those to  the public removes a lot of the uncertainty from the equation.

The public awareness of AI is also quickly growing, and with that the subject is becoming more divisive. While a lot of people are excited about the possibilities, the amount of people who are worried about AI's rapid advance (even including software scientists involved in the field) is also growing. This can result in a negative reception to campaigns using AI, even when they're meant to be light-hearted.
For example, TDE recently released a small [AI-generated video of Jonas Vingegaard as a child](https://twitter.com/JumboVismaRoad/status/1648242844946006016), which was received quite negatively.  
Anticipating fans' reactions is difficult, especially with how volatile the discourse around AI is. Keeping a finger on the public's pulse and looking at potential reception on a case-by-case base is going to be essential to avoid bad press.

Lastly, it's also important to consider how quickly people get used to new technology. ChatGPT has quickly gone from curiosity to the largest-growing application of all time in terms of users, and even those who have nothing to do with AI seem to hardly be surprised at its capabilities anymore. In order to offer fans something unique, TDE will either have to be one of the first to offer them something, which is incredibly difficult without dedicated AI specialist, or try to be the first to find a unique or eye-catching application of existing AI technology.

All the user research I did is collected and discussed in [this report](). 

## What ethical considerations have to be taken into account when working with generative AI?
AI will very likely have a massive impact on our society, enabling us to do and create things unheard of a decade ago. Even more than with most new technology, it could be used to do a great amount of harm, for example with misinformation, spam, or by replacing jobs. I feel like any individual or company developing something with AI has a responsibility to consider how it could be abused.
### Methods
**Literature study:**  
I read up on the current ethical discourse surrounding AI, for example by investigating the safety measures that AI companies have set up. I also tried to get acquainted with related subjects like copyright and portrait rights.
**Ethical check:**  
Unfortunately, the marketing industry isn't exactly renowned for its ethical boundaries, so I investigated the stance of lawmakers and experts (both in the fields of AI and philosphy) on current AI developments.
**Survey:**  
When I surveyed potential users for the third project I also asked them questions about AI in general, giving them hypothetical scenarios and asking them to rate those based on whether or not they believed them to cross ethical boundaries.

### Conclusions

A more thorough examination of the ethics surrounding project 2, as well as a set of ethical guidelines I set up based on my research, can be found [here]().

