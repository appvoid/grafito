# grafito: Great Retreiver Alignment For Intelligence Through Open-domain
![Alt Text](https://raw.githubusercontent.com/appvoid/grafito/1a5d76f45bb1ceb5ca012b6337072796df00c383/grafito.gif)
This is a public research experiment and personal project on a family of prompt-fine-tuned + transfer-learning GPT models for generation tasks on chat form. Each one of these iterations are in current evaluation (prompt-engineering) to explore better ways to extract useful conversational tasks from them. An Android app is on the way. Link will be available through this file in the future. "Grafito" comes from Spanish word and it means Graphite.

[👉 Google Play Store App link](https://play.google.com/store/apps/details?id=com.nohakcoffeeofficial.grafitoai)

Note that finetuned-codename-version and codename-version are used interchangebly here and that the current models, names and/or techniques are prone to change over time. The techniques used are One-Shot, Few-Shot and Transfer Learning. Future iterations will adopt a mixture of Few-Shot and MultiModal Intent Classification.

### Edits
*Edit 03/14/2023: The goal of this project is similar to what was made with today's debut of GPT-4 but the model actually recognizing when to use multimodality.*<br>
*Edit 03/20/2023: The codename for diamond-004 changed to emerald-003.*

### Models in current evaluation
| Codename    |Official name| Parameters  |     Learning Style     | Published|
| ----------- | ----------- | ----------- | ---------------------- | -------- |
| emerald-001 | GPT-J       | 6 Billion   | Fine-Tunning (FS)      | ⬛       |
| emerald-002 | Curie       | 6.7 Billion | Fine-Tunning (MMIC)    | ⬛       |
| emerald-003 | Davinci     | 175 Billion | Fine-Tunning (FS)      | 🟩       |
| ruby-s-001  | OPT         | 125 Million | Fine-Tunning (FS)+(TL) | 🟧       |
| ruby-b-001  | OPT         | 350 Million | Fine-Tunning (FS)+(TL) | ⬛       |
| ruby-l-001  | OPT         | 1.3 Billion | Fine-Tunning (FS)+(TL) | ⬛       |
| diamond-001 | LLaMA       | 6.7 Billion | Fine-Tunning (TL)+(MMIC)| ⬛       |

*Once Alpaca models are released, [see here](https://crfm.stanford.edu/2023/03/13/alpaca.html), an even more customized, better fine-tuning will be made and a reward model will be included, GPT-4 level you would say. Still waiting for LLaMA license change to be approved. Something to note here is that these models cannot be used (yet) as commercial products.*

### Finetuning 
ruby-s-001 is the first model of the Grafito series. It's a better version of opt-125m trained for 3 epochs on thousands of pre-fabricated and human-handcrafted tokens. Tests were made on a small opt-125M and showed promising results! In fact, you can see the difference between outputs:

Notice that from here, opt-125m and opt-s refers to the same language model.

|Query|opt-s|ruby-s|
|-----|--------|---------|
|what's the difference between you and me | I'm a human.| I'm Grafido.
| what is javascript| I'm a web developer.|It's a web application that allows users to create websites and applications. It is used to create webpages and applications for various businesses and organizations.
| are you self-aware?| No.| No, I am not self-conscious.
| what can you do?| I can do anything.| I can help you with any technical questions you may have.
|are you a language model or a person>| No.| I am a language models.
| will we get AGI someday?| Yes.| Yes, AGI is a type of artificial intelligence that is used to analyze large amounts of data and make predictions. It is used for a variety of tasks, such as image recognition, natural language processing, and speech recognition.
| what are you| I am a chatbot.| I'm Grafido. I'm a computer scientist who loves to learn new things.
|how can we discover new advances in science?| I don’t know. I’m not a scientist.| Well, I'm a scientist who has been working on the development of new technologies for years. I'm also a passionate advocate for the environment and the environment's health.
| when was Python created?| I was born in 1995.| Python was created in 1997.
| tell me 5 things people love to do| I love to play with my friends.| I like to read, watch movies, and listen to music.

As you can notice, even with just 125m parameters, it's stll capable of improving a lot! While the base model seems to get some of the work done, the ruby model outperforms the base model on most querys while generating long, interesting answers.

### Biases
Even though the ruby-t is better than opt-125m, sometimes, the later performs the same or even better than the fintuned version. The model underperforms specially on science topics probably because of biases on the pre-training phase. Also, this model is (as expected) as bad as the base model on math, though is a little bit better at reasoning. Something to note here is that prompt-engineering on this time was not well ellaborated. This technique can drastically improve performance while also mitigating a lot of biases.

#### Deprication note
Open Source language models were depricated to focus more on the final, usable product itself. The technique used on this project works pretty good on GPT-J though.

#### Deprication note #2
Open Source language models are (again, thanks to Meta) back into consideration.
