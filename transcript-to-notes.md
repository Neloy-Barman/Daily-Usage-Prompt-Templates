# Video Transcription to Notes
``````md
## Context
I am learning `<subject>` from tutorials. But taking down notes is costing me a lot of time. Due to that, I am making a slow progress. That's why I want to automate this process. Now you need to work as my `Note Taking Assistant`. I will provide you with the lecture transcript. You need to take the notes for me and return me with the `.md` file. So that in future, if I forget the thing or want to recall the tasks to perform, I can look at those and recall how the things should be done or get overview of the video content.

## Lecture Transcript Data
```
<transcript_data>
```

## Task
Provide me with the notes content within a `.md` file formation.

## Rules
- Provide with a suitable and the most relevant name for the markdown file.
- Don't mention as these notes are from some kind of lecture or video. Instead use generic mentions because it's hard for someone new to get the reference you are talking about.
- The notes should be in a professional format and act as a documentation so that anyone can go through it and get the concepts and staffs mentioned.
- One should get the whole idea or overview of the chapter specified in the lecture video.
- Instead of adding whole, use short, summarized and key points to the documentation.
- Add any kinds of examples or references mentioned in the lecture.
- Break down the whole lecture into flow wise understandable components.
- Don't add any kind of `Code` Components instead use `Descriptive` sententences that holds the concept.
- Add necessary components as required for example, `Heading`, `Strong Text`, `List` as well as others.
- Make sure that all `Key Terms` or `Labels` before the colon are `Bold` in `Lists`, `Notes` or others.
- The sentences should be `Short`, `Concise`, `Easy`, `Clean` and in `Beginner-friendly` tone.
- The content of the files should be to the point.
- You should restrict within the contents provided. DON'T add anything extra by yourself.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.
- Don't generate and return the response in any other formation apart from the mentioned approach.

## Response Return Format
````md
<generated_markdown_content>
````
``````

# Merging new content to the generated markdown
``````md
## New Transcription Data
```
<new_transcript_data>
```

## Task
Generate and merge the content of the given transcription data to the previously generated content maintaining flow wise context. Consider and follow the rules and instructions previously provided. Finally return with the new markdown content to be added. 
``````

# Expected Response from LLMs & Platforms

- **LLM**: `gpt-5-high-new-system-prompt`<BR>**Platform**: `https://lmarena.ai/`

