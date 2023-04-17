# Project 2: Sports Icons
TDE will be hosting a Web3 showcase, where they are inviting several high-profile executives in the sports industry to present the opportunities that several new technologies offer. As a part of this conference, they would like to show off something impressive created by generative AI. In keeping with TDE's sports focus, I made a tool that generates video and audio of a famous athlete based on text input, for example allowing you to generate a video of Michael jordan welcoming guests to the conference.

## Research Questions

# Project Overview

## Exploration and Planning

I tried to involve the other TDE employees in the process from the get-go, setting up a meeting with them to discuss possibilities and opportunities for the project, as well as its scope. We discussed the end goal of what I would be making, and how we could best achieve that goal, as well as doing some initial brainstorming.

Since video generation is considerably more difficult than anything text-related, we decided that this project would make use of existing tools, combining several of those into a new application that met the needs of TDE. I also wanted to spend a bit more time on the UX this time, making something that's accessible and easy to use.

Based on feedback, I then tried to create a more extensive planning for this project, which can be found [here](Planning.md).

## First Research

Much of my initial research was into the tools I wanted to make use of. I had to consider quality, usability (for example having an API), as well as cost. The voice generation was fairly easy: I quickly landed on [ElevenLabs](https://www.elevenlabs.io) because of its solid API, fast and high quality voice generation, and relatively low cost.

Video generation proved more difficult; while there are a variety of different tools available, many generate mediocre results. Of the highest quality ones, none that I could find allow you to generate video based on celebrities. After meeting with the stakeholders at TDE to present some options, we decided to generate the video based on an athlete's likeness created with [Midjourney](https://www.midjourney.com), an AI capable of generating lifelike images, currently the best in its category. 
This circuimvents the limitations as well as adding another layer of AI, which serves the projects goal of showing off the technology's capabilities.
For generating the talking head video based on the Midjourney image I decided to use [D-ID](https://www.d-id.com), because it netted the best results out of every tool I experimented with.

Michael Jordan Test .gif![image](https://user-images.githubusercontent.com/9715331/232474418-57b2373b-7ecf-41b7-9321-34cc6345911b.png)
_An early experiment for generating video of Michael Jordan_

## Development

I wanted to create a solid base for my application, which I could iteratively improve upon, as well as use to experiment with. I chose one athlete to focus on; Michael Jordan. If I could get the tool working for one person, it would be easy to add others. 

I started with the voice generation, which was fairly easy to get working, and I was quickly able to get great results. I also used this first prototype to start working on the UI, discussing potential changes with colleagues, which resulted in a more reactive and stripped down UI for the second prototype.

After that, I got started on the video aspect; this was more difficult, both due to the aforementioned restrictions placed on generating videos based on celebrities and the complexity of the API I was using. We experimented with generating portraits using Midjourney, getting as good of a likeness as possible, and used the best results to generate the video.

All that remained was to combine the audio and video generation, and make sure everything was functioning correctly. Some last-minute changes had to be made because one of the endpoints I was using stopped working, but I managed Considering the tool was supposed to be used by TDE, I wanted to make the code clean and easy to adjust, as well as facilitating the addition of more athletes in the future, even without my assistance. 

The repository with the code for the application can be found [here]().

MJ Talking.gif![image](https://user-images.githubusercontent.com/9715331/232474134-f3c1443d-0ace-4b55-84bb-23861692aa1a.png)
_Video generated using the final product_

## Reflection

Focus on MJ
Making use of all the apis, experimenting to see what gives best results
Tried to ask for more feedback during the process
  as a result the app fit better to brief and what TDE was looking for
  more focused, 
  
No time for frontend -> later
  Designs?
Better application due to better communication
Planning helps, but too restrictive and little space for unexpected circuimstances - kanban board next time? 
  For example with unforseen bugs etc, like the malfunctioning endpoint

## Ethical Considerations

Ethics of generating videos of celebrities
  Video of zelensky surrendering to putin
watermnark
