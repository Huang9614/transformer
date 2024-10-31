# Installation
```bash
export PATH=/usr/local/cuda-11.0/bin:$PATH
export CUDA_HOME=/usr/local/cuda-11.0
export LD_LIBRARY_PATH=/usr/local/cuda-11.0/lib64:$LD_LIBRARY_PATH


conda create env -n transformer python=3.8
conda activate transformer

conda install pytorch==1.7.0 torchvision==0.8.1 torchtext==0.8.0 -c pytorch

pip install spacy==3.0.0
python -m spacy download de_core_news_sm
python -m spacy download en_core_news_sm

cd ~/transformer
mkdir data && cd data

wget "https://raw.githubusercontent.com/neychev/small_DL_repo/master/datasets/Multi30k/training.tar.gz"

wget "https://raw.githubusercontent.com/neychev/small_DL_repo/master/datasets/Multi30k/validation.tar.gz"

wget "https://raw.githubusercontent.com/neychev/small_DL_repo/master/datasets/Multi30k/mmt_task1_test2016.tar.gz"

tar -xzvf *.tar.gz
```