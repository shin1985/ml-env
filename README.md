# Purpose

This docker setting is for tring to touch and test some machine learning.

# Installed main softwares

- Tensorflow 1.1.0
- Chainer 1.19.0
- Scikit-learn 0.18.1
- Gensim 2.0.0
- Word2vec 0.9.1
- Numpy 1.12.1
- Pandas 0.19.2
- Jupyter 4.3.0
- Matplotlib 2.0.0
- Mecab latest
- Juman++ 7.01
- Keras 2.0.4
- NLTK 3.2.2
- TFLearn 0.3

and other dependent libraries.


# Password

Please update passwords(default is "ml" for following).

- ml user password
- ipyton password(jupyter_notebook_config.py)


# How to run docker image

    # Build image
    # This image requires more than 13 GB disk space
    docker build -t zuqqhi2/ml-python-sandbox .

    # Run jupyter notebook & tensorboard
    docker run -it -p 8888:8888 -p 6006:6006 zuqqhi2/ml-python-sandbox

    # Login container
    docker run -it -p 8888:8888 -p 6006:6006 zuqqhi2/ml-python-sandbox /bin/bash
    source ~/.bash_profile
    mlact

    # Set japanese locale
    export LANG=ja_JP.UTF-8
    export LC_ALL=ja_JP.UTF-8
    export LC_CTYPE=ja_JP.UTF-8

# Change Log from 1.0.3

- 1.1.0
  - New Library/Tool : Seaborn, TFLearn, TFGraphviz, Tensorboard
  - Others : samples.ipynb to introduce how to use libraries, start_webuis.sh to run jupyter notebook and tensorboard 

# TODO

- Add "hmmlearn" to requirements.txt

# References

- [Jupyter Notebook - Running a notebook server](http://jupyter-notebook.readthedocs.io/en/latest/public_server.html)
- [JUMAN++をPythonから使う](http://qiita.com/riverwell/items/7a85ebf95647eaf18a6c)
- [MecabをUbuntu14.04にインストールして実行してみる](https://foolean.net/p/22)
- [TensorFlowのグラフをJupyter上で可視化する](http://qiita.com/akimach/items/d6d87e9fcdc4800d492a)
