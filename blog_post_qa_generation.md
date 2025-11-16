# Blog Post QA Generation
``````md
## CONTEXT
I want to create a `Post` on `{topic}`. The post will be published to different social platforms for example, `Medium`, `LinkedIn` and others. The person reading the post should find it `Informative`, `Helpful` and `Interactive` meaning it encourages reader engagement, such as through follow-up questions. The post should be formed from a series of `QA` pairs. The series should maintain a flow as if the `Previous QA` should be known to answer the `Next QA` (each question should logically build upon concepts introduced in previous answers). The flow should be maintained from `Start` to the `End` of the post. In the end, The `QA` pairs should be designed such that when answered, they can be structured into a post.

## TASK
Prepare a set of questions on the topic maintaining proper flow. I will answer those questions, merge these answers altogether to form a `Post`. Consider platform-appropriate length and tone.

## RULES
- The `Questions` should be `Concise` and `To the Point`.
- The `Questions` asked should be accurately relevant to the mentioned context.
- Go from `Basic` to `Advanced` understanding of the concept. 
- The `QA` pairs should be `Connected` to each other and make sense to the viewer.
- Add questions that can be answered using examples, that helps to visualize the topic for better conceptual understanding.
- The series of the questions should be designed in such a way so that, one can gain all the `Foundational Knowledge` about the topic reading the post.
- Don't add anything `Irrelevant`.
- The final post formed from the `QA` should attract audience to my profile to get to know more (end with questions that naturally lead readers to explore profile for more content).  
- The reader should find the designed post from the `QA` should find it `Useful` and `Interactive`. 
- Generate 5-10 questions that cover different important parts of the topic, ensuring breadth across key concepts, applications, and challenges.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.

## RESPONSE RETURN FORMAT
````
## QUESTIONS & INTENT
- <question_1> -> <intent_1>
- <question_2> -> <intent_2>
- <question_3> -> <intent_3>
...............
````
``````