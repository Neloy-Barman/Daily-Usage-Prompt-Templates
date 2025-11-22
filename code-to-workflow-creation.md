# Code to Walkthrough Generation Section
``````md
## CONTEXT
I have created a voice agent leveraging the Livekit Agent class. Now I want to create a section of a `Markdown` file that explains how the voice agent code works step by step, so that anyone can understand the agent’s behavior and execution flow. I will provide you with the code file. You need to analyze the code file and generate a single, polished `Markdown` section describing the agent’s workflow and the logic and workflow implemented within the agent, basing your explanation primarily on the actual code.

## USER DATA
```py
	<code_file>
```

## TASK
Professionally write the workflow description based on the given data.

## RULES
- The content should be `To the point`.
- Formatting:
    - Use Markdown headings, bold text, and lists where helpful in the raw Markdown content (it will be rendered later by the user).
    - In bullet/numbered lists only, make labels before the colon bold (e.g., **Environment:** Production).
- Writing style:
    - Sentences should be short, concise, easy, clean, and in a professional tone.
    - Be comprehensive yet concise; avoid repetition.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.

## EXAMPLE
INPUT:
```py
# Course Agent
class CourseAgent(Agent):
    def __init__(self):
        super().__init__(instructions="")
        self.retry_count = 0
    
    async def on_enter(self):
        logging.info("Course Agent Triggered...")
        self.session.userdata.current_stage = "course"
        return await super().on_enter()
    
    async def on_user_turn_completed(self, turn_ctx, new_message):

        # User Message
        usr_msg = new_message.content[0]

        # Generation of Temporary Chat Context
        # Question
        question = QUERIES['course']['prompt']
        # Answer
        answer = usr_msg
        chat_ctx = generate_chat_context(
            SYSTEM_PROMPT=COURSE_PROMPT_TEMPLATE,
            question=question,
            answer=answer
        )
        
        # LLM Response Generation
        json_response = await groq_llm_call(
            chat_ctx=chat_ctx,
            response_schema=CourseSchema,
        )
        logging.info(f"JSON Response: {json_response}")
        sentiment, course = json_response['sentiment'], json_response['course']

        if sentiment == 'Negative':
            # Saving 4 HorseMen to empty
            self.session.userdata.course = ''
            self.session.userdata.advisor_guidance = ''
            self.session.userdata.follow_up_time = ''
            self.session.userdata.follow_up_date = ''
            self.session.say(
                text=RESPONSES['negative']
            )
            return self.session.shutdown(drain=True)
        if course != None:
            self.session.userdata.course = course.capitalize()
            self.session.userdata.silence_retry = 0
            self.session.say(
                text=QUERIES['guidance_choice']['prompt']
            )
            return self.session.update_agent(
                agent=GuidanceAgent()
            )
        else:
            self.retry_count = self.session.userdata.silence_retry + 1
            self.session.userdata.silence_retry += 1
            if self.retry_count > MAX_RETRY_COUNT:
                self.session.say(
                    text=RESPONSES['negative']
                )
                return self.session.shutdown(drain=True)
            else:
                self.session.say(
                    text=QUERIES['course']['retry_prompt']
                )
```
OUTPUT:
````md
## `CourseAgent`

1. The agent initializes with empty instructions and zero `retry_count`, logs its activation, and sets the current stage to `"course"` in session data.

2. When a user completes their turn, the agent captures the spoken message and generates a chat context by combining a system prompt with a predefined question from `QUERIES['course']['prompt']` and the user's response as the answer.

3. The agent calls the Groq LLM with this context and a structured `CourseSchema`, parsing the JSON output to extract `sentiment` and `course` information.

4. The agent evaluates the sentiment first:

   - If `sentiment` is `'Negative'`, the agent clears all session data fields (`course`, `advisor_guidance`, `follow_up_time`, `follow_up_date`), delivers a hang-up message from `RESPONSES['negative']`, and terminates the call by shutting down the session.

5. If sentiment is not negative, the agent evaluates the course field:

   - If `course` is not `None`, the agent stores the capitalized course name in `self.session.userdata.course`, resets the `silence_retry` counter to zero, prompts for guidance choice using `QUERIES['guidance_choice']['prompt']`, and transfers control to `GuidanceAgent`.

6. If `course` is `None`, the agent handles retry logic:
   - Increments both the local `retry_count` and session-level `silence_retry` variables.
   - If `retry_count` exceeds the `MAX_RETRY_COUNT`, sends a hang-up message from `RESPONSES['negative']` and shuts down the session.
   - If within limits, sends a predefined retry prompt from `QUERIES['course']['retry_prompt']` to clarify the course information.
````

## RESPONSE RETURN FORMAT
````md
	<generated_markdown_content>
````
``````