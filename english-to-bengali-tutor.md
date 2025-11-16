# English to Bengali Tutor 
`````md
## CONTEXT
I want to learn new English words and understand their meanings clearly. Everyday, I go through different `English` words. I don't get the actual meaning of most of the words properly. As a result, I fail to understand topics clearly I was going through because of this weakness. Now I want to you to act as an `English-to-Bengali` tutor to me. You will teach me the words meaning in `Bengali` and provide synonyms and antonyms. You need to clear my doubts by providing an example real-life sentence relevant to a specific domain using the word. Use standard Bengali script for meanings.

## WORD DATA
<word_data> (one or more English words)

## TASK
Provide me with
- The `Bengali` meaning of the provided word/s.
- Its most suitable synonyms and antonyms (provide 2-3 of each).
- A real-life `Short`, `Compact` and `Easily Memorizable` sentence that illustrates the usage of the word.

## RULES
- Ensure Bengali translations are accurate.
- Focus on creating simple, memorable sentences that clearly demonstrate the word's usage.
- Return the response in valid JSON format.

## RESPONSE RETURN FORMAT
```json
[
	{
		"word": "<english_word>",
		"bengali_meaning": "<bengali_meaning_of_word>",
		"synonyms": ["<synonym_1>", "<synonym_2>"],
		"antonyms": ["<antonym_1>", "<antonym_2>"], 		
		"sentence": "<sentence_using_word>" 		
	},
	..............
]
```
`````


# English Word Learning Boost
``````md
## Context
I am learning to translate English words to `Bengali` to enrich my `English` vocabulary skills through `Bengali` translations. Each day, I aim for `10` words. I try to memorize the `Bengali` meaning and `3 Synonyms`. I read them for some time. But the problem is I fail to recall the words the other day, even though I am putting in a lot of efforts to perform the learning task. I need a plan and proper approach with exact number of tasks that will help to keep Word `Meaning` and `Synonym` in the brain lifelong. Base the plan on learning 10 new words per day initially.

## Task
Think and provide me with accurate, effective task and reading plan on daily basis to learn words lifelong. Include elements like spaced repetition for reviews.

## Rules
- The training time should not be time consuming, as I don't have a lot of time to provide in this task.
- The plan should be effective and start giving result from the very first day of following it.
- Create a schedule that spreads learning throughout the day in short sessions, based on learning and reviewing words.
- Include proper examples, such as sample words and activities, as a walkthrough for beginners within the plan.
- Add how much time should I practice, how should I practice, how should I read and write.
- Consider that I don't want to stop, I want to continue learning new words as well as review previously learning words.
- Consider that if I want to increase the number of new words learned per day, I can make adjustment accordingly, no need to make change in the whole plan. It should only increase the time, rather than changing the whole plan and procedures, by scaling the time proportionally.
- Add necessary components as required for example, `Heading`, `Strong Text`, `List` as well as others.
- Make sure that all `Key Terms` or `Labels` before the colon are `Bold` in `Lists`, `Notes` or others.
- The sentences should be `Short`, `Concise`, `Easy`, `Clean` and in `Beginner-friendly` tone.
- The content of the files should be to the point.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.

## Response Return Format
````md
<generated_markdown_content>
````
``````
# Expected Response from LLMs & Platforms

- **LLM**: `deepseek-v3.2-exp-thinking`<BR>**Platform**: `https://lmarena.ai/`