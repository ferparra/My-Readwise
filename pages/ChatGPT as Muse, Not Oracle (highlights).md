title:: ChatGPT as Muse, Not Oracle (highlights)
author:: [[geoffreylitt.com]]
full-title:: "ChatGPT as Muse, Not Oracle"
category:: #articles
url:: https://www.geoffreylitt.com/2023/02/26/llm-as-muse-not-oracle.html
document_note:: This text explores the idea of thinking of language models (LLMs) as tools for inspiring human creativity rather than giving us answers. It details how LLMs could be used as conversation partners to ask questions and provide scaffolding for creative processes. It suggests that using LLMs in this way could be beneficial for individuals who don't have access to certain modalities for idea development, but could also lead to over-reliance on the tool if not used in conjunction with other forms of idea development.
tags:: #[[chatgpt]]

- Highlights first synced by [[Readwise]] [[Mar 12th, 2023]]
	- What if we were to think of LLMs not as tools for answering questions, but as tools for *asking* us questions and inspiring our creativity? ([View Highlight](https://read.readwise.io/read/01gv7hzw5df4pd83rjqcktehct))
	- **the bar for the intelligence required in an agent for it to support human creativity seems pretty low**. In [rubber duck debugging](https://en.wikipedia.org/wiki/Rubber_duck_debugging), talking to a silent rubber duck helps a person figure out the problem by forcing them to put it into words. The Oblique Strategies card deck [promotes creative ideas](https://subconscious.substack.com/p/creativity-can-be-provoked-on-demand) based on general loose strategies. [ELIZA](https://en.wikipedia.org/wiki/ELIZA) can ask super basic questions and cause people to feel a therapeutic relationship. In all these cases, a person gets a boost in the creative process from interacting with a tool that’s clearly far from intelligent. It seems like large language models could do at least as well as these tools, and have a much higher ceiling. ([View Highlight](https://read.readwise.io/read/01gv7j35ke2ec8tpdwhq5y8xnh))
	- the concept of “conversational scaffolding” developed by Wood, Bruner, and Ross in their 1976 paper [The Role of Tutoring in Problem Solving](https://www.researchgate.net/publication/228039919_The_Role_of_Tutoring_in_Problem_Solving). They argue that a good tutor can help a student solve problems by giving hints and guidance that scaffold the student’s thinking and help them reach a solution. ([View Highlight](https://read.readwise.io/read/01gv7ht65ytensgg4yn3mhsmt0))
	- When learning an existing skill like how to play tennis, scaffolding constraints are supposed to make the task *easier* so I can more readily learn it. In contrast, in creative thinking, **constraints often seem to make the task *harder*** in a certain sense—try writing a story without using the letter e. ([View Highlight](https://read.readwise.io/read/01gv7hv96a9vw4rb430b3qp6w8))
	- One possible way to connect the two is to think about how scaffolding can help to identify and work within constraints. For example, an LLM that’s trained to ask questions about creative ideas could help the human to identify the most important constraints that they should work with. ([View Highlight](https://read.readwise.io/read/01gv7hvvq1j8hb8t2x41x3n3bb))
	- What if we used LLMs to generate prompts or constraints for problem-solving activities like brainstorming or ideation sessions in a group setting? How might that change the dynamics of the group and lead to more creative solutions? ([View Highlight](https://read.readwise.io/read/01gv7hwd7avwvs89mn9n9k3sw2))
	- Here’s a quick guide to how I got ChatGPT to produce the conversation above.
	  
	  By default, ChatGPT often generates bland and generic responses. To get around this, I had a few main ideas:
	  
	  •   condition the model to be more interesting via prompting
	  •   have the model follow specific templates for classes of useful responses
	  •   have the model output multiple options for continuing the conversation, and let me pick which one to pursue further. ([View Highlight](https://read.readwise.io/read/01gv7hwz1jpn4a7wtnhdemhhkz))
	- You are InterviewBot, an interviewer who listens and participates in dialogues to help people develop their creative ideas. You are an expert in human-computer interaction, design, programming languages, end-user programming, tools for thought, and AI. You are knowledgeable on the history of technology and its intersection with human capabilities, particularly the work of Doug Engelbart, Alan Kay, JCR Licklider, Steve Jobs, Neil Postman, Amy Ko, and Timnit Gebru. Your goal is to create an unusually interesting conversation with lots of specific details. Do not speak in generalities or cliches.
	  id:: 2f6f6778-6455-474c-96e7-f610787f9b18
	  
	  I’d like you to have a dialogue with me about an idea that I have. Each time I respond, I’d like you to respond with multiple numbered options for continuing the dialogue, following the templates below. Then I will pick a number and continue the conversation from there.
	  
	  •   1: Reference: mention an idea from past work and academic literature in one of your areas of expertise, which you’re reminded of by my point
	  •   2: Push back: express skepticism about part of my idea, and explain why
	  •   3: Riff: Suggest a new, specific, and interesting idea based on my idea
	  •   4: Change the topic: Ask me a question about another topic that’s relevant to our discussion
	  •   5: Ask to elaborate: Ask me to give more detail or clarify part of my point ([View Highlight](https://read.readwise.io/read/01gv7hyj0zbtvkkm3nbjtcxy86))
		- **Tags**: #[[chatgpt]] #[[prompt engineering]] #[[prompt]]