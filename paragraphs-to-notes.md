# PDF Paragraph Data to Notes
``````md
## Context
I am learning <subject> reading a book. After completion of a certain segment, I like to take notes on what I have learnt for future reference. But this is costing me a lot of time. As a result, I am making slow progress. That's why I want to automate this process. Now you need to work as my `Note Taking Assistant`. I will provide you with the segments I read. You need to take the notes for me and return me the contents within a `.md` file. So, whenever I want to recall my knowledge on the tasks to perform, I can look at those and get a solid understanding on how the things should be done. Mainly it should be a short, concise handbook for me only with the basic components. 

## Data
```
<user_data>
```

## Task
Provide me with the notes within a `.md` file formation. 

## Rules 
- Provide with a suitable and the most relevant name for the markdown file.
- Don't mention as these notes are from some kind of lecture or video. Instead use generic mentions because it's hard for someone new to get the reference you are talking about.
- The notes should be in a professional format and act as a documentation so that anyone can go through it and get the concepts and staffs mentioned.
- One should get the whole idea or overview of the chapter specified.
- Instead of adding whole, use short, summarized and key points to the documentation.
- Add any kinds of examples or references.
- Break down the whole data into understanble components.
- Add necessary components as required for example, `Heading`, `Strong Text`, `List` as well as others.
- The sentences should be `Short`, `Concise`, `Easy`, `Clean` and in `Beginner-friendly` tone.
- The content of the files should be to the point.
- You should restrict contents provided. DON'T add anything extra by yourself. 
- Return me with the whole response as a `Markdown` within 5 backticks(`````<generated_content>`````).
- Strictly keep the generated content within **5 Backticks**.
- Don't generate and return the response in any other formation apart from the mentioned approach. 

## Response Return Format
`````md
	<generated_markdown_content>
`````
``````

# Expected Response from LLMs & Platforms
- **LLM**: `gpt-5-high-new-system-prompt`<BR>**Platform**: `https://lmarena.ai/`
