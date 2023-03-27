# TDE Internship Portfolio
Rik Jansen

Updated 23-3-23

## First Weeks

The first two weeks were spent getting to know the company, and getting to grips with my assignment. Early on, me and my coordinator at TDE decided that we would split the internship into four seperate projects, all focused on a different theme and subject within the field of generative AI. This way, I could explore more different avenues, as well as giving me the opportunity to swerve in direction if an exciting new direction suddenly opened up. Considering how fast the field of AI is moving nowadays, this is a very real possibility, and halfway through the internship TDE might suddenly think of something interesting I could be doing.

I tried to get a good idea of the current state of AI, and what the possibilities were. Based on this research, I outlined several concepts and themes I was interested in exploring, and together with my TDE coordinator we picked a few that we were most interested in. None of these were fixed, leaving the option for new ideas open.

## Project 1: Podcast Summarizer

I made an application that automatically transcribes and summarizes a podcast. It's intended to be used by the journalists of RacingNews365, a Formula 1 news site, who get a lot of their news from podcasts. This tool could save them a lot of time, by extracting just the most pertinent info, and indicating whether or not the podcast is worth listening to. Me and my TDE coordinator decided on this project as a good introduction to using generative AI models, as audio and text is a relatively simple subject within the field.

### Exploration and Planning

From the start, I had a pretty clear view of my assignment, and what my end result would be used for. TDE had already discussed using tools like these with RacingNews365, and could tell me what the requirements were. I set up some [requirements](/Project_1/Requirements.md), made a first setup of the project plan, and started work.

### Research into Transcription Models

For this first project, I wanted to implement the AI models myself, to obtain a good base from which I could work the rest of the internship. To choose the right AI model for the job, I did some research into their strenghts and weaknesses, which is collected in this [research report](/Project_1/AI_Model_Research.md).

### Prototyping and Implementation

I quickly set up some simple prototypes that allowed me to play around with different transcription and summarization models, and get some experience with their implementation. These same prototypes were used to run some basic tests on the models, to pick the one that best suited my needs. Most of the development time of this project was spent on the backend, implementing the models and getting them to work together, as well as working on language options and a simple UI.

The source code, as well as the Jupyter Notebooks I used for early testing, of the project can be found [here](https://github.com/RikJansenTU/PodcastSummarizer).

I set up and ran a small demo to show the result of my work to TDE, both to show the other employees some of the possiblities for AI (especially implementing models of your own), as well as get some feedback on what could be improved for next project. In general, I think they were quite satisfied with the result, even if my way of working within the company could be improved (see reflection below)

I also met with one of the devops developers of TDE to discuss setting up a space on the TDE domain to host all of my finished demos.

### Future Steps and User Testing

I spent a lot of time working on the backend, and the frontend and UI of the project turned out pretty basic as a result. For my next project, I'd like to focus a bit more on making an accessible and usable application.

Unfortunately, I didn't have time to implement a feature for looking up timestamps in the podcast for certain parts of the summary. While I do have a good idea of how I could implement this, I ran out of time, and decided that this feature wasn't as important as getting the base application running well.

I want to offer the tool I created to RacingNews, and hopefully have them use it for a few weeks, after which I can hold some short interviews to get their throughts on it. It'll be interesting to see if they make use of it, and to hear their feedback.

### Reflection and Feedback

Overall, setting up and making use of the AI models proved easier than expected, which allowed me to get going with prototyping and experimentation quite quickly. 

One thing I want to improve during the next project is my planning. While I did outline what I wanted to work on at the start of the assignment, I didn't make a very extensive or detailed list. For the next project, I want to plan out my activities more precisely, documenting exactly how long I think each activity will take. This will also make it easier for my coordinators, at both Fontys and TDE, to see what I'm working on.

Being more open about my work was a point of feedback I got from my TDE internship coordinator. When I get started on a project, I tend to dive in by myself, and I sometimes struggle letting other people know what I'm working on or asking for help. While I'm pretty happy with the technical end result of this first project, I think I can still take a lot of steps in how I act as part of TDE.
I think this struggle with involving others is partially due to the different work environment, suddenly being part of a larger team but without explicitly working on the same things. Starting next project, I want to take a more proactive approach in gathering feedback, asking for help, and showing off my work, for example by planning meetings with other team members to discuss my progress.

## Project 2: Sport Icons

### Exploration and Planning

Based on feedback, I tried to set up a more elaborate planning for this prokect, which was as follows:

*Week 1 (20-3 t/m 24-3): reflectie project 1, afbakening, planning, en eerste design project 2.*
Reflectie project 1, eerste opzet portfolio. 1 dag
Eerste meeting en planning project 2. Maandag 27-3
Onderzoek naar opties en technologie project 2. 1 dag.
Tweede meeting voor bespreking planning project 2. Vrijdag 31-1.
Bijwerken weekupdate, portfolio, projectplan voor project 2. 1 dag.
Eerste design voor frontend in Figma. 1 dag.
*Week 2: (27-3 t/,m 31-3): Eerste prototype, feedback*
Een eerste prototype opzetten, dat alleen stem-simulatie bevat. 2 dagen
Feedback-meeting prototype. Woensdag 29-3
Tweede prototype met stem-simulatie. 1 dag.
Verfijnen design frontend gebaseerd op eerste feedback. 1 dag.
Onderzoek naar gezicht-simulatie. 1 dag.
*Week 3: (3-4 t/m 7-4): Iteratie*
Tweede prototype: eerste implementatie gezicht-simulatie. 3-4 dagen.
Feedback-meeting prototype 2.
Eerste implementatie frontend gebaseerd op design. 1 dag.
Feedback-meeting frontend.
*Week 4: (11-4 t/m 14-4): Afronding*
Laatste prototype, puntjes op de i zetten. 2-3 dagen.
Eindrapportage schrijven, resultaten verzamelen. 1 dag.
Demo en presentatie aan TDE. 1 dag.
  
## Final

Presentation at TDE about AI etc
