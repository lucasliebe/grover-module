 Grover

## General Information

This Repository is a Fork of the Original Grover Project:

(aka, code for [Defending Against Neural Fake News](https://arxiv.org/abs/1905.12616))

Grover is a model for Neural Fake News -- both generation and detection. However, it probably can also be used for other generation tasks.

Visit the original project page at [rowanzellers.com/grover](https://rowanzellers.com/grover), [the AI2 online demo](https://grover.allenai.org), or read the full paper at [arxiv.org/abs/1905.12616](https://arxiv.org/abs/1905.12616).

![teaser](https://i.imgur.com/VAGFpBe.png "teaser")

## What's in this repo?

Functionality copied from the [source repository](https://github.com/rowanz/grover) and modified to work with newer Python/ Tensorflow Versions and be called as methods instead of from command line.

* Code for the Grover generator (in [lm/](lm/)).
* Code for the Grover discriminator in [discrimination/](discrimination/). Without much changing, you can run Grover as a discriminator to detect Neural Fake News.
* Code for generating from a Grover model, in [sample/](sample/).

## Setting up your environment

Please note that this repository currently does not support GPU acceleration since the package versions have been changed in comparison to the original project.

Use `pip install requirements.txt` to download the required packages.
Afterwards download the model using `python download_model.py base` or `large` or `mega`

Misc notes/tips:
* If you have a lot of projects on your machine, you might want to use an anaconda environment to handle them all. Use `conda create -n grover python=3.6` to create an environment named `grover`. To enter the environment use `source activate grover`. To leave use `source deactivate`.

Congrats! Now you can use Grovers functionalities that are contained in this repository!
