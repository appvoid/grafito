# grafito: Great Retreiver Alignment For Intelligence Through Open-domain
![Alt Text](https://raw.githubusercontent.com/appvoid/grafito/1a5d76f45bb1ceb5ca012b6337072796df00c383/grafito.gif)
This is a public research experiment and personal project on a family of prompt-fine-tuned + transfer-learning GPT models for generation tasks on chat form. Each one of these iterations are in current evaluation (prompt-engineering) to explore better ways to extract useful conversational tasks from them. An Android app is on the way. Link will be available through this file in the future. "Grafito" comes from Spanish word and it means Graphite.


~~[👉 Google Play Store App link](https://play.google.com/store/apps/details?id=com.nohakcoffeeofficial.grafitoai)~~
App is temporaly down.

Note that finetuned-codename-version and codename-version are used interchangebly here and that the current models, names and/or techniques are prone to change over time. The techniques used are One-Shot, Few-Shot and Transfer Learning through LoRA.

### Edits
*Edit 03/20/2023: The codename for diamond-004 changed to emerald-003.*<br>
*Edit 04/04/2023: Cerebras introduced their new models.*<br>
*Edit 05/24/2023: Things have changed a lot, now heading towards to lora models.* <br>
*Edit 05/26/2023: Things have changed (again), now heading towards to "native" training.* 

### Models
| Model       |Official name | Parameters  |     Learning Style     | Sequence Length | Epochs           | Learning Rate         | Dataset           | Published |
| ----------- | -----------  | ----------- | ---------------------- | --------------- | ---------------- | --------------------- | ----------------- |---------- |
|[obsidian-000](https://huggingface.co/appvoid/obsidian-000)|dlite-v1|124 Million| Fine-Tunning (FS)+(TL) | 512             | 2                | 5e-4                  | anthropic-hh-rlhf | 🟩        |
| ruby-s-001  |gpt2          | 160 Million | Fine-Tunning (FS)+(TL) | Coming soon...  | Coming soon...   | Coming soon...        | Coming soon...    | 🟧        |
| ruby-m-001  |gpt2          | 355 Million | Fine-Tunning (FS)+(TL) | Coming soon...  | Coming soon...   | Coming soon...        | Coming soon...    | ⬛        |
| ruby-l-001  |gpt2          | 1.5 Billion | Fine-Tunning (FS)+(TL) | Coming soon...  | Coming soon...   | Coming soon...        | Coming soon...    | ⬛        |

*Note that obsidian models are lab models while the others are the official ones*

### Zero-Shot Benchmark
Notice that from here, dlite refers to the orignial dlite-v1 language model.

| query |  dlite  |  obsidian  |
| ----- | ------- | ---------- |
|what's the difference between you and me | I'm not sure. You're asking about my relationship with my parents. What do they have in common? They both work hard to make a living, but their families are different. Do you think that is fair enough? | I'm a vegetarian, but I’m not sure if that”s right or wrong.  It‪s important to understand that vegetarians are omnivores, meaning they eat plant-based foods, and it―ll be important for them in order of importance.  For example, eating a plant-based diet is important because it helps to maintain a healthy weight, reduce inflammation from chronic
| what is javascript| JavaScript is a scripting language used to create webpages. It is designed for use with HTML, CSS and JavaScript.|JavaScript is a programming language used to create websites and applications. It is a powerful, interactive scripting language that can be used for many different tasks, including web development, HTML/CSS, JavaScript code execution, and more.  It is also a popular choice among developers and designers due its ability of creating complex user interfaces and user-friendly design.
| are you self-aware?| Yes, I am. | Yes, I'm self aware.  Self awareness is a mental state that involves recognizing and understanding the external world around us as we are or can be.  It’s a way of thinking about our own thoughts and feelings, which is why I think it's important to have a sense for ourselves in order not become overwhelmed with negative thoughts or emotions.  Selfawareness also helps me to recognize and understand the limitations
| what can you do?| You could try to find a restaurant near you and ask them about their menu. They might also offer discounts or special offers for customers who visit the store regularly. Additionally, they may have helpful FAQs available on their website that explain more about your options. Finally, if you're looking for something specific, there are plenty of great restaurants in town with similar offerings from other cities. So make sure to check out these places| I'm here to help you with your homework.  Here are some things you should know:   1) You’re not allowed in the classroom, and 2)(I don't want to be in the classroom).
|are you a language model or a person| I am an English Language Model. | I'm not a language model, but I am an expert in the field of language modeling.  I specialize mainly on the development and implementation aspects for languages such as Python (Python is a programming language), Java/C++, C# etc., which are all very popular tools for developing native applications.  I also have extensive experience with languages such ASL, C++11, Swift, and C#.
| will we get AGI someday?|We may have to wait a few more years for the completion of our project. However, it is likely that in 2023, we can expect to see an announcement about the development of a new AI-powered robot called the "Robot of Tomorrow". This robotic robot could be used to assist humans with tasks such as cleaning and maintenance, helping them stay healthy and productive, or even providing medical advice.| I think that the answer is likely to be yes.  It’s a long time since humans have been able genetically programmed for this purpose, and it”s still very early days in human evolution.  There are many potential applications of AGI, and there are some potential risks associated with its use, but I believe that AGI is an important tool for humanity to continue to develop and improve.
| what are you| I am writing to share my experience with the new product. It has been a while since I have used it, but this time around I'm excited to try it out!  | I'm sorry, I’m not sure.  What do your parents have in common?  Are they married or divorced and have children?  Do their parents have any special needs that you want to know more about?  Is there anything else I can help you with?
|how can we discover new advances in science?| Scientists have been working on a variety of scientific discoveries over the past few decades. These include the development and application of new technologies, such as artificial intelligence (AI), computer vision to study complex phenomena, and the development or development of new methods for analyzing data. Additionally, scientists have developed new ways of studying and interpreting large amounts more accurately than ever before | I think it's important to research and understand the scientific method, and to use the tools available to do so.  It’s also important for us not only as scientists but also as citizens of our own planet.  We need a better understanding that is more accurate than ever before about what is happening in the world today - and this is why I believe that there are many opportunities for progress in science.
| when was Python created?| PyCharm released version 2.0 of Python in May 2018. It is a fork from PyChang and provides support for the latest features, such as support for multiple languages, support for Python 3.4+, and support with Python 4+. Additionally it supports Python 5.x, which is an updated version of Python that has improved performance and bug fixes.| Python was created in 1989.  It is a programming language that has been around since the early 1990s, and it is still widely used today as an alternative to Java or C++.  Python is a popular choice for many different applications, including web development, scripting languages like PythonScript (Python), and web frameworks like Django.
| tell me 5 things people love to do| Read, listen and laugh. 5. Learn something new every day.  6. Take a break from the mundane and focus on the important.  7-8 hours of relaxation time is essential for overall wellbeing. 9.-10 minutes of deep breathing are necessary for optimal sleep quality. 11 - 12 hours of physical activity can help reduce stress levels. | I'm going on a vacation, and my favorite activities are swimming in the ocean, reading a book, playing a game of chess or something.  It's also great for relaxation and relaxation time.  You can find lots more information about this here: https://www!instagram.com/pinterest/.

As you can notice, even with just 124m parameters, it's stll capable of improving a lot! While the base model seems to get some of the work done, the obsidian model outperforms the base model on most querys while generating long, interesting answers.

### Biases
Even though the obsidian is better than dlite-v1 answering questions, sometimes, the later performs the same or even better than the fintuned version. The model underperforms specially on science topics probably because of biases on the pre-training phase. Also, this model is (as expected) as bad as the base model on math, though is a little bit better at reasoning. Something to note here is that prompt-engineering on this time was not well ellaborated. This technique can drastically improve performance while also mitigating a lot of biases. Long-form generation limited its abillitie to write code or lists.
