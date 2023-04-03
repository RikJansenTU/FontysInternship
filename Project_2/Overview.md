# Project 2: Sports Icons
TDE will be hosting a Web3 showcase, where they are inviting several high-profile executives in the sports industry to present the opportunities that several new technologies offer. As a part of this conference, they would like to show off something impressive created by generative AI. In keeping with TDE's sports focus, I made a tool that generates video and audio of a famous athlete based on text input, for example allowing you to generate a video of Michael jordan welcoming guests to the conference.

## Exploration and Planning

I tried to involve the other TDE employees in the process from the get-go, setting up a meeting with them to discuss possibilities and opportunities for the project, as well as its scope. We discussed the end goal of what I would be making, and how we could best achieve that goal, as well as doing some initial brainstorming.

Since video generation is considerably more difficult than anything text-related, we decided that this project would make use of existing tools, combining several of those into a new application that met the needs of TDE. I also wanted to spend a bit more time on the UX this time, making something that's accessible and easy to use.

Based on feedback, I then tried to create a more extensive planning for this project, which can be found [here](Planning.md).

## First Research

Much of my initial research was into the tools I wanted to make use of. I had to consider quality, usability (for example having an API), as well as cost. The voice generation was fairly easy: I quickly landed on [ElevenLabs](www.elevenlabs.io) because of its solid API, fast and high quality voice generation, and relatively low cost.

Video generation proved more difficult; while there are a variety of different tools available, many generate mediocre results. Of the highest quality ones, none that I could find allow you to generate video based on celebrities. After meeting with the stakeholders at TDE to present some options, we decided to generate the video based on an athlete's likeness created with [Midjourney](www.midjourney.com), an AI capable of generating lifelike images, currently the best in its category. 
This circuimvents the limitations as well as adding another layer of AI, which serves the projects goal of showing off the technology's capabilities.
For generating the talking head video based on the Midjourney image I decided to use [D-ID](www.d-id.com), because it netted the best results out of every tool I experimented with.

# Ethical Considerations

Ethics of generating videos of celebrities
watermnark
