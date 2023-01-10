 Grover
##### UPDATE, Sept 17 2019. We got into NeurIPS (camera ready coming soon!) and we've made Grover-Mega publicly available without you needing to fill out the form. You can download it using [download_model.py](download_model.py).

(aka, code for [Defending Against Neural Fake News](https://arxiv.org/abs/1905.12616))

Grover is a model for Neural Fake News -- both generation and detection. However, it probably can also be used for other generation tasks. 

Visit the official project page at [rowanzellers.com/grover](https://rowanzellers.com/grover), [the AI2 online demo](https://grover.allenai.org), or read the full paper at [arxiv.org/abs/1905.12616](https://arxiv.org/abs/1905.12616). 

![teaser](https://i.imgur.com/VAGFpBe.png "teaser")

## What's in this repo?

Functionality copied from the [source repository](https://github.com/rowanz/grover) and modified to work with newer Python/ Tensorflow Versions and be called as methods instead of from command line.

* Code for the Grover generator (in [lm/](lm/)).
* Code for the Grover discriminator in [discrimination/](discrimination/). Without much changing, you can run Grover as a discriminator to detect Neural Fake News.
* Code for generating from a Grover model, in [sample/](sample/).

## Setting up your environment

There are a few ways you can run Grover according to the original repository:
* **Generation mode (inference)**. This requires a GPU because I wasn't able to get top-p sampling, or caching of transformer hidden states, to work on a TPU.
* **LM Validation mode (perplexity)**. This could be run on a GPU or a TPU, but I've only tested this with TPU inference.
* **LM Training mode**. This requires a large TPU pod.
* **Discrimination mode (training)**. This requires a TPU pod.
* **Discrimination mode (inference)**. This could be run on a GPU or a TPU, but I've only tested this with TPU inference.

Use `pip install -r requirements-gpu.txt` if you're installing on a GPU, or `pip install requirements-tpu.txt` for TPU.
Afterwards download the model using `python download_model.py base` or `large` or `mega`

Misc notes/tips:
* If you have a lot of projects on your machine, you might want to use an anaconda environment to handle them all. Use `conda create -n grover python=3.6` to create an environment named `grover`. To enter the environment use `source activate grover`. To leave use `source deactivate`.

Congrats! Now you can use Grovers functionalities that are contained in this repository!
