# Bert-based-keyword-extraction
Keyword extraction system based on BERT

## Usage
1. Clone this repository and install Huggingface's library `transformers`
2. Change the parameters accordingly in `experiments/base_model/params.json`.
3. For training, run the command `!python train.py --data_dir data/task1/ --bert_model_dir model/ --model_dir experiments/base_model` (change to `task2` for other semeval task, keyphrase classification)
4. For eval, run the command, `!python evaluate.py --data_dir data/task1/ --bert_model_dir model/ --model_dir experiments/base_model --restore_file best`

## Results
Task 1 (keyphrase boundary identification):
|   |precison   |recall   |f1-score   |support   |
|---|---|---|---|---|
|I   |29.87   |49.95   |37.38   |921   |
|avg/total   |29.87   |49.95   |37.38   |921   |

Task 2 (Keyphrase Classification):
BIO format is used for this task
|          | Precision | Recall | F1-score | Support |
|----------|-----------|--------|----------|---------|
| Process  | 0.4734    | 0.5207 | 0.4959   | 870     |
| Material | 0.4958    | 0.6617 | 0.5669   | 807     |
| Task     | 0.2125    | 0.2537 | 0.2313   | 201     |
| Avg      | 0.4551    | 0.5527 | 0.4981   | 1878    |
