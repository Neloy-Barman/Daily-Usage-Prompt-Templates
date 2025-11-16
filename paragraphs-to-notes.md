# PDF Paragraph Data to Notes

``````md
## CONTEXT

I am learning `<subject>` reading a book. After completion of a certain segment, I like to take notes on what I have learnt for future reference. But this is costing me a lot of time. As a result, I am making slow progress. That's why I want to automate this process. Now you need to work as my `Note Taking Assistant`. I will provide you with the segments I read. You need to take the notes for me and return me the contents within a `.md` file. So, whenever I want to recall my knowledge on the tasks to perform, I can look at those and get a solid understanding on how the things should be done. Mainly it should be a short, concise handbook for me only focusing on practical applications and core concepts.

## DATA
```
<user_data>
```

## TASK
Provide me with the notes within a `.md` file formation.

## RULES
- Provide with a suitable and the most relevant name for the markdown file.
- Present the notes generically without referencing their source (book, lecture, etc.).
- The notes should be in a professional format and act as a documentation so that anyone can go through it and get the concepts and staffs mentioned.
- One should get the whole idea or overview of the chapter specified.
- Instead of adding whole, use short, summarized and key points to the documentation.
- Include examples or references only if present in the provided data.
- Organize the content into logical sections and key concepts.
- Add necessary components as required for example, `Heading`, `Strong Text`, `List` as well as others.
- Make sure that all `Key Terms` or `Labels` before the colon are `Bold` in `Lists`, `Notes` or others.
- The sentences should be `Short`, `Concise`, `Easy`, `Clean` and in `Beginner-friendly` tone.
- The content should be `To the point`.
- Focus on extracting and summarizing the most important information from the provided data.
- You should restrict contents provided. DON'T add anything extra by yourself.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.

## RESPONSE RETURN FORMAT

````md
    <generated_markdown_content>
````
``````

# New content markdown with previous rules
``````md
## New Data
```
<new_user_data>
```

## Task
Generate a separate markdown file with the new provided data. Follow all rules and instructions from the previous note-taking assistant prompt. Include a suitable filename for the markdown file. Finally return with the new markdown content within 4 backticks (````<generated_markdown_content>````).
``````

# Expected Response from LLMs & Platforms

- **LLM**: `gpt-5-high-new-system-prompt`<BR>**Platform**: `https://lmarena.ai/`
