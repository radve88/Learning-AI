# Learning-AI

 1. [CLS] Token Embedding as Sentence Summary
Transformer models like BERT prepend a special token [CLS] to every input.

The output at the position of [CLS] (i.e., index 0) is used as the embedding that summarizes the entire sentence.

That’s why you do:


outputs.last_hidden_state[:, 0, :]
to extract that summary vector.

✅ 2. Embedding Shape
The shape of outputs.last_hidden_state is:


(batch_size, sequence_length, hidden_size)
For example, if you process one sentence at a time (batch_size = 1) and you use a base BERT model (hidden_size = 768), then:


outputs.last_hidden_state[:, 0, :] → (1, 768)
Then .squeeze() makes it (768,), which is a single vector per sentence that you can use in traditional ML models.

 1. [CLS] Token Embedding as Sentence Summary
Transformer models like BERT prepend a special token [CLS] to every input.

The output at the position of [CLS] (i.e., index 0) is used as the embedding that summarizes the entire sentence.

That’s why you do:


outputs.last_hidden_state[:, 0, :]
to extract that summary vector.

✅ 2. Embedding Shape
The shape of outputs.last_hidden_state is:


(batch_size, sequence_length, hidden_size)
For example, if you process one sentence at a time (batch_size = 1) and you use a base BERT model (hidden_size = 768), then:


outputs.last_hidden_state[:, 0, :] → (1, 768)
Then .squeeze() makes it (768,), which is a single vector per sentence that you can use in traditional ML models.

