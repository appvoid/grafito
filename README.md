# grafito: Great Retreiver Alignment For Intelligence Through Open-domain
![Alt Text](https://raw.githubusercontent.com/appvoid/grafito/1a5d76f45bb1ceb5ca012b6337072796df00c383/grafito.gif)
This is a public research experiment and personal project on a set of prompt-fine-tuned GPT-series models for generation tasks on chat form. Each one of these models are in current evaluation (prompt-engineering) to explore better ways to extract useful conversational tasks from them. Custom prompts and an Android app is on the making using the prompt-fine-tuned model pt-diamond-001-beta and will be released here, link will be available through this file in the future. "Grafito" comes from Spanish word and it means Graphite. It's powered by the glorious banana's API!

Note that finetuned-codename-version and codename-version are used interchangebly here and that the current models, names and/or techniques are prone to change over time.

### Models in evaluation / fine-tunning
| Codename    |Official name| Parameters  |     Learning Style     | State |
| ----------- | ----------- | ----------- | ---------------------- | ----- |
| Diamond     | GPT-J       | 6 Billion   | Few-Shot               | 🟩 |
| Ruby        | GPT Neo     | 2.7 Billion | Fine-Tunning (pending) | ⬛ |
| Emerald     | GPT Neo     | 1.3 Billion | Fine-Tunning           | ⬛ |

Progress will made top-to-bottom, from the highest performant to the lowest, this way it is ensured that we are getting the most from each model. The main goal of the project is to get an align system that understand NLP tasks and performs those tasks using few-shot templates. Also, to get the lower performant models as close as possible to Diamond performance.

### Observations

#### (12/16/2022)
**Emerald/Ruby performance**

- Sometimes Emerald performs better than Ruby. This fact implies that there are different "sweet spots" for each mdoel even when the same model is feeded on the same data with different number of parameters.

**Diamond**
- When fine-tunning Diamond on basic few-shot (Q:A:) pairs, rather than additional context like "This is a chatbot that does...", it consistently gives better results than other interview-like styles. Specially when Top P = 1. Mentioned setting is default now.
- Does pretty weird at math. When asked: "2 plus 5", "2+5", "Two plus five", answers "8." or "Eight.". It gets close but fails.
- Also, encoded memory as context makes the chatbot ocassionally repetitive which is bad for memory since it will "think" that he should say the same thing forever. A proper solution remains in experimenting with temperature which is even worse for accuracy most of the time. The only solution that seems to be plausible is to fill the chatbot with as much optimal context as posible and append to the tail of the context two or three sections of relevant chat history.
