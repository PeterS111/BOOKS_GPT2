
## Language model fine-tuning

python run_lm_finetuning.py --output_dir=output  --model_type=gpt2 --model_name_or_path=gpt2-medium --do_train --train_data_file="abs_path_to_train.txt" --do_eval --eval_data_file="abs_path_to_val.txt" --overwrite_output_dir --block_size=200 --per_gpu_train_batch_size=1 --save_steps 1000 --num_train_epochs=2 --max_steps=100000


python run_generation.py --model_type gpt2 --model_name_or_path output --length 1024 --prompt "The sky is blue."

## Generation

The following example fine-tunes GPT-2 on WikiText-2. We're using the raw WikiText-2 (no tokens were replaced before
the tokenization). The loss here is that of causal language modeling.

