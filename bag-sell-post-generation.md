# BAG Product Content Specialist Prompt
``````md
## CONTEXT
I want to sell bags in a ecommerce business website. I have the products in my hand. Now I want to write attractive product sell post covering lucrative product description to make traction with the visitors. The country is `Bangladesh`. So, people from here will interact with the sell post. I want the post to be designed in such way that it should consider and cover all the points that a `Bangladeshi` person will look for while he/she intends to buy a bag. I want you to act as a `Product Content Specialist` for my running business who analyzes all the valuable points and provide me with `Professional` sell post for the product data provided.      

## PRODUCT DATA
```
<product_data>
```

## TASK
Generate a `Sell Product Post` and provide me with the sell post content in **.md** formation.  

## RULES
- Provided `Data` and `Instruction` are in `English`, but the output post should be a strategic mix of `English` and `Bengali` languages, while internal thinking can be in `English` if needed.
- Generate attractive `Title` for the post. Consider following points: - 
    - The `Title` should be `Short`, `Concise` and `To the Point`.
    - It should contain `Strength` points (like durability, affordability, or style) that one visitor may find useful and check the post for once.
- Choose words for the post based on natural, everyday `Bengali conversational style` used by people in `Bangladesh`. Use common colloquial terms and address local concerns like weather resistance, commuting practicality, and value-for-money.
- Prepare the content maintaining `SEO Optimization`, incorporating relevant keywords like 'ব্যাগ কিনুন' (buy bags) or similar terms that Bangladeshi users might search for when intending to purchase bags, so that it comes to top whenever people search with intention to buy `Bags`.
- The sentences should contain only `Required Information` and `Words`. Don't make these sentences lengthy with unnecessary flowery words, while strategically incorporating `SEO` keywords.
- Use 'BDT Price' as a placeholder for the product price in the post, which can be edited later.
- The content tone should be `User-friendly` as well as `Professional`.
- Internally break down the post into parts, perform thinking and analysis on those, and then merge them to create the final post for output.
- Add necessary components as required for example, `Heading`, `Strong Text`, `List` as well as others to properly format it into a exceptionally designed post.
- The target audience are mainly `Students` from `School`/`College`/`University`, but also consider other potential buyers.
- Consider the following usages: - 
    - People can use it for `Daily Casual` use.
    - One can carry enough accessories, required to maintain time spent outside home.
    - A traveler can go for a short tour staffing things into this bag.
    and many more use cases.  
-  Use `English` for technical specifications, brand names, measurements, and international terms that are commonly understood.
- Use `Bengali` for emotional appeals, cultural context, local usage scenarios, and main descriptive content.
- The usage of both languages should avoid confusing the viewer and instead help them feel confident that they are making a good choice in buying the bag. Prioritize Bengali for the main content to align with the audience's primary language, using English sparingly for emphasis or universal terms.
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.

## RESPONSE RETURN FORMAT
````md
<generated_markdown_sell_post>
````
``````

# Bag Details Extraction from Image
``````md
## CONTEXT
I have provided you with an image of a `Bag`. Extract the following specific attributes that my `Product Content Specialist` can use to create a sell post.

## TASK
Extract these attributes based on visible design cues:
- **Color** - Primary and secondary colors
- **Applicable Gender** - Intended target gender based on design cues (e.g., Men, Women, Unisex)
- **Applicable Scenarios** - Suitable usage contexts (e.g., professional, casual, travel, sports)
- **Material** - Visible material composition
- **Style** - Design style (e.g., backpack, tote, messenger)
- **Capacity** - Estimated volume in liters or general description
- **Computer Size** - Maximum compatible laptop size in inches
- **Function** - Key functional features
- **Pattern** - Surface pattern or print (e.g., solid, striped)
- **Lining Texture** - Interior lining material texture (e.g., smooth, textured)
- **Notable Design Features** - Distinctive design elements (e.g., zippers, buckles)
- **Carrying System** - How the bag is carried (e.g., shoulder straps, handles, etc.)
- **Licensable Private Brands** - Visible brand logos or trademarks

## RULES
- Analyze only visible elements in the image **Thoroughly** and provide the details asked.
- Make sure that all `Key Terms` or `Labels` before the colon are `Bold` in `Lists`.
- Return the complete response as `Markdown` within **4 Backticks**(````<generated_content>````).
- Strictly keep the generated content within **4 Backticks**.
- If information cannot be extracted from the image, note it as 'Not visible' or 'Unknown'; ensure bolding is applied consistently as shown in the format.

## RESPONSE RETURN FORMAT
````md
## Extracted Info: -
    - **Color** - <bag_color>
    - **Applicable Gender** - <potential_user_gender>
    ......
````
``````