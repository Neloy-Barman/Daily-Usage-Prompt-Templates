# Image Generation compositing Product Cutout and Reference

``````md
## CONTEXT
I have selected a reference image and a product image. I have removed the background from the product image and created a cutout of the product in PNG format. I have placed the product cutout on the reference image, making the product the subject. I am passing this composite-in-progress to an Image Generation/Editing Model. I want all other elements to remain the same as in the reference image. What should I write in the placeholder `Describe how you want to edit this image` to achieve the result I mentioned? You need to provide me with a prompt for that.

## TASK
Generate a prompt to fill in the placeholder `Describe how you want to edit this image`.

## RULES
- The prompt should instruct to composite and harmonize the `Product Cutout` (subject) into the reference image (scene).
- It should keep the reference image’s Style Specification, Background Details, Lighting Style, Camera POV/Angle & Composition, Aspect Ratio & Lens characteristics, Depth of Field, and overall realism/dynamism unchanged.
- The generated image from the prompt should be a new composition that merges the cutout as the subject into the reference image’s scene/atmosphere.
- The prompt content should be Short, Concise, and To the point.
- The prompt should be Optimized and Generic.
- Respect the current subject placement (position, scale, orientation) and ensure seamless integration (clean edges, matched color/exposure/white balance, appropriate shadows/reflections, and perspective alignment) with the reference scene.
- Return the prompt as a single paragraph wrapped in exactly **4 backticks (````<prompt>````)**.

## RESPONSE RETURN FORMAT
````md
    <prompt>
````
``````

# Response
### gpt-5.1-high
```md
Integrate the placed product cutout seamlessly into this image while preserving the reference photo’s original style, background details, lighting, camera POV/angle and composition, aspect ratio and lens characteristics, depth of field, and overall realism. Keep the product’s current position, scale, and orientation unchanged and only refine edges and blending. Match the product’s color, exposure, contrast, sharpness, and white balance to the environment, and add natural, correctly oriented shadows and any needed reflections consistent with the existing light and perspective so it looks natively part of the scene. Do not modify, move, add, or remove any other elements.
```

### deepseek-v3.2-exp-thinking
```md
Seamlessly composite the product cutout into the reference image, preserving all original scene elements, style, lighting, camera perspective, composition, aspect ratio, lens characteristics, and depth of field. Ensure harmonious integration with matched colors, exposure, white balance, clean edges, realistic shadows, reflections, and correct perspective alignment.
```

### gemini-3-pro
```md
Seamlessly blend the product into the existing scene. Generate realistic contact shadows, reflections, and lighting interactions. Match the environment's color grading and exposure while preserving the original background and style.
```

### grok-4.1-thinking
```md
Seamlessly composite and harmonize the foreground product cutout as the main subject into the exact scene, preserving its current position, scale, orientation, and clean edges; perfectly match lighting, color, exposure, white balance, shadows, reflections, and perspective to the reference background; keep the entire background, composition, camera angle, POV, depth of field, aspect ratio, lens characteristics, style, realism, and atmosphere 100% unchanged.
```