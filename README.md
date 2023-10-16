![FireFly_Background](https://github.com/Firefly-HackGT/firefly-pages/assets/59548615/f1a795ed-0173-4260-877f-a27bb64dac06)

### [Project Demo](https://devpost.com/software/firefly-jl91pg)

### Our Mission
Just like fireflies light up the night, our project, Firefly, is here to help students and professors brighten their learning journey. Imagine a classroom where sometimes it's hard for students to grasp what's being taught. They might feel a little nervous about asking for help, and so they stay quiet. They might not even know enough about the lecture material to be able to ask a question. This means the teacher might not know when the students need extra help.

That is where Firefly comes in. It is like a friendly guide, helping students express how well they understand a lesson, using a scale from 1 to 5. Teachers can see which areas need a little more attention, so they can explain these topics in more detail. With Firefly, we are creating a space where everyone can learn together and where no one has to feel lost or left behind. Together, we're turning on the light of knowledge, making sure no one feels in the dark about their learning.

### Inspiration

Imagine this all too common scenario: the whole class has no idea what the professor is talking about. The professor stops and asks, "Any questions?". However, you and everyone else are so lost that you don't even know what you don't know. And the professor says, "_Really_... okay guess you guys understand" and keeps going. We've experienced this frustration in our own classes, so we came up with Firefly: the only way to say you do or don't understand to your professor with only the click of a button.

### What it does
Firefly is a website that allows professors to get a temperature check about how the class feels about each part of a lecture. The professor simply visits: thefirefly.tech and creates a section for every topic covered in lecture (with the ability to add an associated description for slide numbers, resources, etc.). Then students join with the session ID and provide a rating from 1-5 about how confident they feel about the given section topic. As the professor advances through the lecture, he gets real-time data on how his students feel about the current section and he simply hits the next arrow key to allow students to rate the next section. At the end, the professor gets a report on class ratings per section and each student gets informed on what sections they struggled with and should review later. Both students and professors can check on their dashboard for all of their previous lectures and given ratings or average ratings respectively.

### How we built it
Our front-end is built using React, Javascript, HTML, and SASS and runs on a Vercel server that communicates with our Python backend through websockets (using the websockets library)  to provide real-time updates for all users during the lecture. Our Python backend runs on a Render server as a websockets web service. At the end of each lecture, all of the data collected by the back-end is thrown into our NoSQL MongoDB database to be accessed when needed on the professor and student dashboard. All of our servers continuously deploy from our Github repositories that are contained within our [Firefly Github Organization](https://github.com/Firefly-HackGT). We also created a stylized README that is hosted through Github Pages.

### Challenges we ran into
Though many of us have worked with HTTP REST services, in order to make this a real-time application we needed to learn websockets. This was an initial roadblock until we found Python's websockets library and created an initial example project. With the knowledge we gained from the example project, we were able to implement websockets into our own project. When we were making the Github Pages, we ran into issues with building the components of the theme, but they were overcome with some quick research. None of us had experience with cloud databases, so we faced the challenge of having to learn and implement MongoDB Atlas within the timeframe. Luckily, there are a plethora of online resources so we were able to implement the database with only a few setbacks. We also struggled to find a service to host our dynamic website with continuous deployment from GitHub, but we ended up finding Vercel and it was smooth sailing from there.

### Accomplishments that we're proud of
We are proud of adding a NoSQL database, which none of us had experience in prior to this project. We are very proud of having built a full dynamic website from frontend to backend within the span of about a day. We are also proud of having learned about and incorporated websocket development, MongoDB, full stack development, product design, and simple but straightforward UI for simple ease of use.

### What we learned
As mentioned earlier, we learned many new technologies, platforms, and frameworks while creating our project, such as MongoDB, websockets, Vercel, SASS, and React. We also learned the full process of creating a fully-functioning website, from brainstorming ideas to designing the frontend and backend to testing our product and making changes where necessary.

### What's next for Firefly
We have plenty of ideas for additional features which we weren't able to get to due to the time constraint, so we would definitely start there. One additional feature we would love to implement include providing the student with study resources for topics they were less confident in. We would also like to allow students to ask questions on the current section, allow other students to upvote the questions they find helpful, and track more statistics such as the amount of questions asked per section. Additionally, we want to use AI models to find what subjects students struggle with the most by identifying keywords in low-scoring lecture sections. Firefly would also be more accessible if we integrated account tracking systems such as the ability to log in through an existing Google account. Finally, we would like to work with TAs to test Firefly and get feedback on what the project does right and wrong from the people who would likely interact with it the most.
