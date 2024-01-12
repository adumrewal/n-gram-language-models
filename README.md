## Whart are n-gram language models?
N-gram language models are a type of statistical language model used in natural language processing and computational linguistics. These models are based on the frequency of n-grams in a given text or corpus. An n-gram is a contiguous sequence of n items, which can be characters, syllables, or more commonly, words.

The most common type of n-gram model is the bigram (2-gram) model, where sequences of two adjacent words are considered. However, n-grams can be of any length, and higher-order n-grams such as trigrams (3-grams) or more are also used, although they become computationally more intensive.

### Here's a brief overview of how n-gram language models work:

#### Tokenization:

The first step involves breaking down a given text into individual units, which are often words. This process is called tokenization.

#### Counting n-grams:

The model then counts the frequency of occurrences of each n-gram in the text. For example, in a bigram model, it counts how often each pair of consecutive words appears.

#### Probability Estimation:

The frequency information is used to estimate the probability of the occurrence of a specific n-gram given the preceding (n-1) items. This probability is often calculated using the formula:

$$
P(w_n | w_1, w_2, ..., w_{n-1}) = \frac{\text{Count}(w_1, w_2, ..., w_n)}{\text{Count}(w_1, w_2, ..., w_{n-1})}
$$

- \(w_1, w_2, ..., w_n\): Words in the sequence.
- `Count(w_1, w_2, ..., w_n)`: The count of the n-gram in the text.
- `Count(w_1, w_2, ..., w_{n-1})`: The count of the (n-1)-gram (preceding sequence) in the text.

This formula is fundamental to estimating the likelihood of a specific n-gram occurring given the preceding (n-1) items, forming the basis of n-gram language modeling.

#### Language Modeling:

The probabilities of various n-grams are then used to model the likelihood of a given sequence of words occurring in a language. This is particularly useful for tasks such as speech recognition, machine translation, and text generation.

---

N-gram models have several advantages, including simplicity and efficiency, but they also have limitations. One notable limitation is the inability to capture long-range dependencies between words since they only consider a fixed number of preceding words.

More sophisticated language models, such as neural language models (e.g., transformer-based models like GPT-3), have gained popularity in recent years, as they can capture more complex patterns and dependencies in natural language data compared to traditional n-gram models.
