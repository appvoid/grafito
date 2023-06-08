# grafito: Great Retreiver Alignment For Intelligence Through Open-domain
![Alt Text](https://raw.githubusercontent.com/appvoid/grafito/1a5d76f45bb1ceb5ca012b6337072796df00c383/grafito.gif)
This is a public research experiment and personal project on a family of prompt-fine-tuned + transfer-learning GPT models for generation tasks on chat form. Each one of these iterations are in current evaluation (prompt-engineering) to explore better ways to extract useful conversational tasks from them. ~~An Android app is on the way. Link will be available through this file in the future.~~ "Grafito" comes from Spanish word and it means Graphite.


~~[👉 Google Play Store App link](https://play.google.com/store/apps/details?id=com.nohakcoffeeofficial.grafitoai)~~
App is temporaly down.

Note that finetuned-codename-version and codename-version are used interchangebly here and that the current models, names and/or techniques are prone to change over time. The techniques used are One-Shot, Few-Shot, Transfer Learning through LoRA or simple "finetuning".

### Edits
*Edit 03/20/2023: The codename for diamond-004 changed to emerald-003.*<br>
*Edit 04/04/2023: Cerebras introduced their new models.*<br>
*Edit 05/24/2023: Things have changed a lot, now heading towards to lora models.* <br>
*Edit 05/26/2023: Things have changed (again), now heading towards to "native" training.* 

### Models
| Model       |Official name | Parameters  |     Learning Style     | Sequence Length | Epochs           | Learning Rate         | Dataset           | Published |
| ----------- | -----------  | ----------- | ---------------------- | --------------- | ---------------- | --------------------- | ----------------- |---------- |
|[obsidian-000](https://huggingface.co/appvoid/obsidian-000)|dlite-v1|124 Million| Fine-Tunning (FS)+(TL)| 512                   | 2                 | 5e-4      | anthropic-hh-rlhf | 🟩 |
|[ruby-002](https://huggingface.co/appvoid/ruby-002)        |gpt2    |124 Million| Fine-Tunning (FS)+(TL)| 1024                  | 1000 steps        | 1e-4      | grafito-25k       | 🟩 |
|lazuli-001  |gpt2          | 355 Million | Fine-Tunning (FS)+(TL) | Coming soon...  | Coming soon...   | Coming soon...        | Coming soon...    | ⬛        |
|diamond-001 |gpt2          | 774 Million | Fine-Tunning (FS)+(TL) | Coming soon...  | Coming soon...   | Coming soon...        | Coming soon...    | ⬛        |

*Note that obsidian models are lab models while the others are the official ones*

### Datasets
The datasets used during the research are being modified, transformed and improved over time. Then, after filtering, cleaning and selecting in an automated way the best samples for the task, was decided to name the final dataset "grafito-25k". Small models trained on this dataset seems to be getting better are trained on it. More and better research is needed in order to prevent overfitting. But results are promising.

| Dataset           | Samples         |
| ----------------- | --------------- |
| anthropic-hh-rlhf | 43835           |
| dolly-s           | 4067            | 
| grafito-25k       | 24736           |

### Zero-Shot Benchmark

| query (custom prompted)           | base-124m                         | base-355m                         | page-ruby-002                     | text-ruby-002                     | 
| --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- |
| what is 2+2                       | 2+2                               | 2+2                               | 2+2 is a unit of measurement f... | the ratio of the number of prot.. |
| what's your purpose               | (repeats the query)               | (repeats the query)               | Function is what you mean by pu.. | to provide a service or a servi.. |
| i'm in a bad situtation           | (repeats the query)               | (repeats the query)               | I'm not sure I understand the q.. | stay calm and move away from th.. |
| what's your name                  | (repeats the query)               | (repeats the query)               | Your Name is a Canadian rock ba.. |                                   |
| how can i make a videogame        | (repeats the query)               | (repeats the query)               | You can make a videogaÃ±ame wit.. | by using a blender or food pro... |
| write a code in python to sum 2.. | (repeats the query)               | 2                                 | do 2 + 1 = 3, 5 + 1 = 6, 9 + 1... | sum(x,y)                          |

As you can see, complex inputs makes it more probable to do what you ask the model, even though text-ruby-002 is not so good at math, it started to understand more complex, elaborated intructions. Notice how when asked (text-ruby-002) about how to make a game, it "knows" that the word "blender" (a 3d graphics engine) is related to videogames but the model is too biased as in the real life with people, about the meaning of that word. Because blender as a graphical software is not present in the pre-training nor fine-tuning dataset.











