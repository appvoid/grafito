# GPT Model Alignment

Alignment is necessary to create a system that follows human intentions. On this particular project, we are creating a multimodal AI that generates several answers and choose the best one based on thruthfulness.

### Experiment 001

#### Brute-force Multimodal Feeback

In our first try, we are going to use three models to generate plausible yet factual answers from a zero-shot prompting. We are going to use a task finetuned version of opt-1.3B, a finetuned version of bart on the mnli dataset and another finetuned version of bart on long form question answering.

First, the OPT model will generate answers till certain threshold is met. We set the threshold to 7 possible answers with at least a 90% accuracy on bart-mnli. Then, we will feed the candidates to a second model, bart-lfqa, which will be generating the actual answwer.

### Results

Based on experiments with bart-mnli, we found that tolerable thresholds for this model start at a 74% of truthfulness based on 61 samples though sometimes gets stucked thinking a good answer.
But after an extended realtime testing, we discover high, innacurate responses, which means that there were not enough samples test it.
But for most of the answers, it was a really good trade-off between speed to get responses and the quality measured.

As a final word, this method it's pretty easy to replicate on every model but there is a huge trade off between speed and performance: by the time we get a good answer if at all, any user will stop generating the answer.
