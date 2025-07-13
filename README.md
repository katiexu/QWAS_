# QWAS_

## Installation: 
conda create -n QWAS python=3.9 

conda activate QWAS 

cd QWAS 

pip install --editable .

## Usage: 
**Attention: Remember to clear the “states” folder and “weights” folder each time you switch tasks.**
1) To search for the best architecture for a specific task, run: 
python MCTS.py –task ‘task_name’ --pretrain ‘filename’
2) To pretrain the classifier for a specific task, run: 
python MCTS_pretrain.py –task ‘task_name’ --output ‘filename’
3) To reproduce the results from the paper, use the following commands:
   - MNIST/FASHION:
      - python MCTS_pretrain.py –task MNIST/FASHION -output pre_mnist_4
      - python MCTS.py –task MNIST/FASHION – pretrain pre_mnist_4
   - MNIST-10/FASHION-10:
      - python MCTS_pretrain.py –task MNIST-10/FASHION-10 -output pre_mnist_10
      - python MCTS.py –task MNIST-10/FASHION-10 –pretrain pre_mnist_10 
   - MOSI:
      - python MCTS.py –task MOSI 
4) The best searched architectures across the whole process are saved 
in the file “result_XXX_fine.csv”.
5) We have saved the initial weights of VQC as ‘init_weight_mnist’, 
‘init_weight_mnist_10’and ‘base_weight_MOSI’for these three 
tasks.  To save time, you can rename them to ‘ini_weight’ in the 
‘init_weights’ folder to start the corresponding task.
6) The MOSI dataset can be accessed at the link below and needs to be copied 
to the folder /data:
https://onedrive.live.com/?authkey=%21AJG4VoHVmTglOoI&id=886B00DEF7AEF48D%21547927&cid=886B00DEF7AEF48D&parId=root&parQt=sharedby&o=OneUp  
