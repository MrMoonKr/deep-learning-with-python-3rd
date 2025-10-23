# 책 부록 소스 프로젝트 입니다

- 직무 교육( OJT, On the job Training )을 위해서 생성.  
- 진행중( WIP, Work on Progress ).  
  + ...


## 책 관련 링크  

<img src="https://m.media-amazon.com/images/I/61Xt0FMZ2jL._SY522_.jpg" alt="" height="256px" align="right">

- [Deep Learning with Python, Third Edition [ 원서 ]](https://www.manning.com/books/deep-learning-with-python-third-edition)  

- [Deep Learning with Python, Third Edition [ 온라인 버전 ]](https://deeplearningwithpython.io/chapters/)  

- [Deep Learning with Python, Third Edition [ 번역서 없음 ]](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=365783770) 

- [ 케라스 창시자에게 배우는 딥러닝 2nd [ 번역서 ]](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=299812465)  


## 시스템 환경  

- 시스템 ( Computer System )  

  - AMD Ryzen 9 7900X 12-Core Processor
  - 32G RAM
  - NVIDIA Geforce RTX 3060 12GB
  - SSD 2TB
  - Windows 11 64bit Korean

- 파이썬 ( Python 3.12 )  

  - [Python Download](https://www.python.org/downloads/)  
    - [v3.12.0 for Windows](https://www.python.org/ftp/python/3.12.0/python-3.12.0-amd64.exe)  
    - [v3.11.9 for Windows](https://www.python.org/ftp/python/3.11.9/python-3.11.9-amd64.exe)  

- 파이썬 가상환경 ( venv )

  > 윈도우즈 파워쉘 실행 정책 변경 필요할 수 있음
    ```
    $ Get-ExecutionPolicy
    $ Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
    $ Get-ExecutionPolicy
    ```
  > venv 환경 실행
    ```
    $ python -m venv .venv
    $ .venv/Scripts/Activate.ps1 
    $ (.venv-) python --version
    $ (.venv-) pip --version
    ```


---
---
---

# Companion notebooks for Deep Learning with Python

This repository contains Jupyter notebooks implementing the code samples found in the book [Deep Learning with Python, third edition (2025)](https://www.manning.com/books/deep-learning-with-python-third-edition?a_aid=keras&a_bid=76564dff)
by Francois Chollet and Matthew Watson. In addition, you will also find the legacy notebooks for the [second edition (2021)](https://www.manning.com/books/deep-learning-with-python-second-edition?a_aid=keras&a_bid=76564dff)
and the [first edition (2017)](https://www.manning.com/books/deep-learning-with-python?a_aid=keras&a_bid=76564dff).

For readability, these notebooks only contain runnable code blocks and section titles, and omit everything else in the book: text paragraphs, figures, and pseudocode.
**If you want to be able to follow what's going on, I recommend reading the notebooks side by side with your copy of the book.**

## Running the code

We recommend running these notebooks on [Colab](https://colab.google), which
provides a hosted runtime with all the dependencies you will need. You can also,
run these notebooks locally, either by setting up your own Jupyter environment,
or using Colab's instructions for
[running locally](https://research.google.com/colaboratory/local-runtimes.html).

By default, all notebooks will run on Colab's free tier GPU runtime, which
is sufficient to run all code in this book. Chapter 8-18 chapters will benefit
from a faster GPU if you have a Colab Pro subscription. You can change your
runtime type using **Runtime -> Change runtime type** in Colab's dropdown menus.

## Choosing a backend

The code for third edition is written using Keras 3. As such, it can be run with
JAX, TensorFlow or PyTorch as a backend. To set the backend, update the backend
in the cell at the top of the colab that looks like this:

```python
import os
os.environ["KERAS_BACKEND"] = "jax"
```

This must be done only once per session before importing Keras. If you are
in the middle running a notebook, you will need to restart the notebook session
and rerun all relevant notebook cells. This can be done in using
**Runtime -> Restart Session** in Colab's dropdown menus.

## Using Kaggle data

This book uses datasets and model weights provided by Kaggle, an online Machine
Learning community and platform. You will need to create a Kaggle login to run
Kaggle code in this book; instructions are given in Chapter 8.

For chapters that need Kaggle data, you can login to Kaggle once per session
when you hit the notebook cell with `kagglehub.login()`. Alternately,
you can set up your Kaggle login information once as Colab secrets:

 * Go to https://www.kaggle.com/ and sign in.
 * Go to https://www.kaggle.com/settings and generate a Kaggle API key.
 * Open the secrets tab in Colab by clicking the key icon on the left.
 * Add two secrets, `KAGGLE_USERNAME` and `KAGGLE_KEY` with the username and key
   you just created.

Following this approach you will only need to copy your Kaggle secret key once,
though you will need to allow each notebook to access your secrets when running
the relevant Kaggle code.

## Table of contents

* [Chapter 2: The mathematical building blocks of neural networks](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter02_mathematical-building-blocks.ipynb)
* [Chapter 3: Introduction to TensorFlow, PyTorch, JAX, and Keras](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter03_introduction-to-ml-frameworks.ipynb)
* [Chapter 4: Classification and regression](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter04_classification-and-regression.ipynb)
* [Chapter 5: Fundamentals of machine learning](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter05_fundamentals-of-ml.ipynb)
* [Chapter 7: A deep dive on Keras](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter07_deep-dive-keras.ipynb)
* [Chapter 8: Image Classification](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter08_image-classification.ipynb)
* [Chapter 9: Convnet architecture patterns](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter09_convnet-architecture-patterns.ipynb)
* [Chapter 10: Interpreting what ConvNets learn](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter10_interpreting-what-convnets-learn.ipynb)
* [Chapter 11: Image Segmentation](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter11_image-segmentation.ipynb)
* [Chapter 12: Object Detection](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter12_object-detection.ipynb)
* [Chapter 13: Timeseries Forecasting](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter13_timeseries-forecasting.ipynb)
* [Chapter 14: Text Classification](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter14_text-classification.ipynb)
* [Chapter 15: Language Models and the Transformer](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter15_language-models-and-the-transformer.ipynb)
* [Chapter 16: Text Generation](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter16_text-generation.ipynb)
* [Chapter 17: Image Generation](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter17_image-generation.ipynb)
* [Chapter 18: Best practices for the real world](https://colab.research.google.com/github/fchollet/deep-learning-with-python-notebooks/blob/master/chapter18_best-practices-for-the-real-world.ipynb)
