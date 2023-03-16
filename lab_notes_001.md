# Training data notes

### Quora answers

https://www.quora.com/If-I-would-have-a-1GB-text-file-txt-approximately-how-many-words-would-it-include
As a rule of thumb we could take the average as 5 letters, plus a space. How many bytes you need for a word depends on the encoding. 
If you are using pure ASCII, 1 per character, then you will need 6 bytes per word. 
On the other hand if you are using Unicode, that will typically use 2 bytes per character, so 12 bytes per word.
Assuming a binary gigabyte (1,073,741,824 bytes), then at 6 bytes per word you could store about 179 million words. 
Using Unicode, half of this, that is 89.5 million words.

### OpenAI Tokenizer webpage

https://platform.openai.com/tokenizer
A helpful rule of thumb is that one token generally corresponds to ~4 characters of text for common English text. 
This translates to roughly ¾ of a word (so 100 tokens ~= 75 words).

### Analysis

We set 1 Gigabyte (1 Million Kilobytes) of Unicode plain text to roughly 90 million words.
Then we take the approximated formula of OpenAI's tokenizer, and we can find that,
if we have have 100 words, we will get 125 tokens, meaning that we that for each word, we are getting 1.25x tokens.


1 GB = ~90 million words = ~11.25 million tokens
