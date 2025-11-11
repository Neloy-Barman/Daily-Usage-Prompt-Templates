# AI ART Reproduction Prompt Fine-Tuning
_Upload the image along with the prompt._

``````md
## CONTEXT
I have provided you with an image generated using an image generation model. 

The actual prompt for the image is: -
```
<original_prompt>
```

Now I am trying to create a prompt by myself analyzing the image in detail. My goal is recreate the provided image using the prompt written by me. The following one is my prompt: -
```
<reproduced_prompt>
```

## TASK
Observe and analyze the image and my prompt deeply. Find out the gaps in my prompt. Think whether the image can be recreated using my prompt or not. Tell me how I should have written the prompt. Finally provide me with the optimized and fine-tuned prompt along with the mistakes as key points.

## RESPONSE RETURN FORMAT
`````md
 ## Fine-Tuned Prompt
 <fine_tuned_prompt>
 
 ## Key points missing
- <point_1>: <details_of_point_1>
- <point_2>: <details_of_point_2>
...........
- <point_n>: <details_of_point_n>
`````
``````