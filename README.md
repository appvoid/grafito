# grafito
This is a public research experiment and personal project on a set of prompt-fine-tuned GPT-series models for generation tasks on chat form. Each one of these models are in current evaluation (prompt-engineering) to explore better ways to extract useful conversational tasks from them. Custom prompts and an Android app on the making using the prompt-fine-tuned model finetuned-diamond-001-beta will be released here, link will be available through this file in the future. 

Note that finetuned-codename-version and codename-version are used interchangebly here.

### Models in evaluation / fine-tunning
| Codename    |Official name| Parameters  | Accuracy    |
| ----------- | ----------- | ----------- | ----------- |
| Opal        | Bloom       | 1 Billion   | Coming soon | 
| Emerald     | GPT Neo     | 1.3 Billion | Coming soon |
| Ruby        | GPT Neo     | 2.7 Billion | Coming soon |
| Diamond     | GPT-J       | 6 Billion   | In progress |

Progress will made top-to-bottom, from the highest performant to the lowest, this way it is ensured that we are getting the most from each model. The main goal of the project is to get the lower performant models as close as possible to Diamond performance.

### Observations (16/12/2022)

**Emerald/Ruby performance**

- Sometimes Emerald performs better than Ruby. This fact implies that there are different "sweet spots" for each mdoel even when the same model is feeded on the same data with different number of parameters.

**Diamond**
- When fine-tunning Diamond on basic few-shot (Q:A:) pairs, rather than additional context like "This is a chatbot that does...", it consistently gives better results than other interview-like styles. Specially when Top P = 1. Mentioned setting is default now.
- diamond-001 does pretty weird at math. When asked: "2 plus 5", "2+5", "Two plus five", answers "8." or "Eight.". It gets close but fails.
