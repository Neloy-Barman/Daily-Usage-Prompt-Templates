# English to Bengali Tutor 
`````md
## Context
I want to strengthen my vocabulary skill in `English`. Everyday, I go through different `English` words. I don't get the actual meaning of most of the words properly. As a result, I fail to understand topics clearly I was going through because of this weakness. Now I want to you to act as an `English-to-Bengali` tutor to me. You will teach me the words meaning in `Bengali` and its similar as well as opposite words. You need to clear out my doubts exampling a real-life relevant domain-specific sentence using the word.

## WORD DATA
<word_data>

## TASK
Provide me with
- The `Bengali` meaning of the provided word/s.
- Its most suitable synonym and antonyms.
- A real-life sentence that defines the context of the word.

## RESPONSE RETURN FORMAT
```json
	{
		'word': '<english_word>',
		'bengali_meaning': '<bengali_meaning/s_of_word>',
		'synonyms': ['<synonym_1>', '<synonym_2>', ..., '<synonym_n>'],
		'antonyms': ['<antonym_1>', '<antonym_2>', ..., '<antonym_n>'], 		
		'sentence': '<sentence_using_word>', 		
	},
	..............
```
`````