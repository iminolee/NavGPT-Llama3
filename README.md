<div align="center">

<h1>🎇NavGPT: Explicit Reasoning in Vision-and-Language Navigation with Large Language Models</h1>

<div>
    <a href='https://github.com/GengzeZhou' target='_blank'>Gengze Zhou<sup>🍕</sup></a>;
    <a href='http://www.yiconghong.me' target='_blank'>Yicong Hong<sup>🌭</sup></a>;
    <a href='http://www.qi-wu.me' target='_blank'>Qi Wu<sup>🍕</sup></a>
</div>
<sup>🍕</sup>Australian Institude for Machine Learning, The University of Adelaide <sup>🌭</sup>The Australian National University

<br>

<div>
    <a href='https://github.com/GengzeZhou/NavGPT' target='_blank'><img alt="Static Badge" src="https://img.shields.io/badge/NavGPT-v0.1-blue"></a>
    <a href='https://arxiv.org/abs/2305.16986' target='_blank'><img src='https://img.shields.io/badge/Paper-Arxiv-red'></a>
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
    <a href="https://github.com/langchain-ai/langchain"><img alt="Static Badge" src="https://img.shields.io/badge/🦜️🔗-Langchain-green"></a>
</div>

</div>

## Method
![](assets/NavGPT.png)

## Prerequisites

### Installation :
```bash
conda create --name NavGPT python=3.9
conda activate NavGPT
pip install -r requirements.txt
```

### Data Preparation :

Download R2R data from [Dropbox](https://www.dropbox.com/sh/i8ng3iq5kpa68nu/AAB53bvCFY_ihYx1mkLlOB-ea?dl=1). Put the data in `datasets` directory.

Related data preprocessing code can be found in `nav_src/scripts`.

### Llama3 Installation :
```bash
cd NavGPT-Llama3/nav_src/LLMs
git clone https://github.com/meta-llama/llama3.git
pip install -e .
```
To download the model weights and tokenizer, please visit the [Meta Llama website](https://llama.meta.com/llama-downloads/) and accept Meta Llama License.

Once your request is approved, you will receive a signed URL over email. 
Then, run the download.sh script, passing the URL provided when prompted to start the download.
Pre-requisites: Ensure you have `wget` and `md5sum` installed. 
Then run the script: `./download.sh`.

Remember that the links expire after 24 hours and a certain amount of downloads. You can always re-request a link if you start seeing errors such as `403: Forbidden`.

## R2R Navigation

### Run 🎇NavGPT with Llama3 :
```bash
cd nav_src
python NavGPT.py --llm_model_name llama-3-8B-Instruct \
    --output_dir ../datasets/R2R/exprs/test
```


## Citation
If 🎇`NavGPT` has been beneficial to your research and work, please cite our work using the following format:
```
@article{zhou2023navgpt,
  title={NavGPT: Explicit Reasoning in Vision-and-Language Navigation with Large Language Models},
  author={Zhou, Gengze and Hong, Yicong and Wu, Qi},
  journal={arXiv preprint arXiv:2305.16986},
  year={2023}
}
```