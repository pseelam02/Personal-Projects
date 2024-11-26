Building and training my first bigram transformer nueral network. This is a decoder-only model, that does not explicitly answer questions, rather it autocompletes Shakespeare. This is because I skipped out on the finetuning stages after the model was trained. 


Model Parameters - 10.78 Million
Model Hyperparameters - 
batch_size = 64 # how many independent sequences will we process in parallel?
block_size = 256 # what is the maximum context length for predictions?
max_iters = 5000
eval_interval = 500
learning_rate = 3e-4
device = 'cuda' if torch.cuda.is_available() else 'cpu'
eval_iters = 200
n_embd = 384
n_head = 6
n_layer = 6
dropout = 0.2

This is an amazing video I used to learn about how to actually implement a generative pre-trained transformer.
https://www.youtube.com/watch?v=kCc8FmEb1nY

The research paper that started everything:
https://arxiv.org/pdf/1706.03762

To Do:
Train this model on a different corpus of text data!

A diagram of the decoder only architecture from Transformers:
![image](https://github.com/user-attachments/assets/860fad93-fba3-48bd-a0f2-0c1eb979c7cd)

