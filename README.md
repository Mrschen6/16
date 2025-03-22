# 16
 ## :wrench: Installation
 ```
 # clone this repo
 git clone https://github.com/Mrschen6/16.git
 
 # create environment
 conda create -n NTIRE2025RWFR python=3.10
 conda activate NTIRE2025RWFR
 
 # install python dependencies
 pip install -r requirements.txt
 
 # install basicsr
 python basicsr/setup.py develop
 ```
 
 ## :ferris_wheel: Test
 ```bash
 CUDA_VISIBLE_DEVICES=0 python test.py --valid_dir [path to val data dir] --test_dir [path to test data dir] --save_dir [path to your save dir] --model_id 0
 ```
 
 ## 💈 Eval
 ```sh
 python eval.py \
 --mode "test" \
 --output_folder "/path/to/your/output_dir_test" \
 --lq_ref_folder "/path/to/input_LQ_dir" \
 --metrics_save_path "./IQA_results" \
 --gpu_ids 0 \
 --use_qalign True 
 ```
