## Introduction
DALIB is a domain adaptation library based on pure PyTorch with high performance and friendly API. The supported algorithms currently include:

- [Domain-Adversarial Training of Neural Networks 
(DANN)](https://arxiv.org/abs/1505.07818)
- [Deep Adaptation Networks (DAN)](https://arxiv.org/abs/1502.02791)
- [Joint Adaptation Networks (JAN)](https://arxiv.org/abs/1605.06636)
- [Conditional Adversarial Domain Adaptation 
(CDAN)](https://arxiv.org/abs/1705.10667)
- [Maximum Classifier Discrepancy (MCD)](https://arxiv.org/abs/1712.02560)
- [Adaptive Feature Norm (AFN)](https://arxiv.xilesou.top/abs/1811.07456)
- [ Margin Disparity Discrepancy (MDD)](https://arxiv.org/abs/1904.05801)

## Installation

DALIB is currently hosted on [PyPI](https://pypi.org/project/dalib/). It requires Python >= 3.6. You can simply install dalib with the following command:

```bash
    pip install -i https://test.pypi.org/simple/ dalib
```

You can also install with the newest version through GitHub:

```bash
pip install git+https://github.com/JunguangJiang/DALIB.git@master
```

After installation, open your python console and type

```python
import dalib 
print(dalib.__version__)
```

If no error occurs, you have successfully installed DALIB.
    
## Documentation
You can find the tutorial and API documentation on the website: [DALIB API](https://dalib.readthedocs.io/en/latest/index.html)

Also, we examples in the directory `examples`. A typical usage is 
```shell script
# Train a DANN on Office-31 Amazon->Webcam task using ResNet 50.
# Assume you have put the datasets under the path `data/office-31`, 
# or you are glad to download the datasets automatically from the Internet to this path
python examples/dann.py data/office31 -d Office31 -s A -t W -a resnet50  --epochs 20
```

In the directory `examples`, you can find all the necessary running scripts to reproduce the benchmarks with specified hyper-parameters.

## Contributing
We appreciate all contributions. If you are planning to contribute back bug-fixes, please do so without any further discussion. If you plan to contribute new features, utility functions or extensions, please first open an issue and discuss the feature with us.

## Disclaimer on Datasets

This is a utility library that downloads and prepares public datasets. We do not host or distribute these datasets, vouch for their quality or fairness, or claim that you have license to use the dataset. It is your responsibility to determine whether you have permission to use the dataset under the dataset's license.

If you're a dataset owner and wish to update any part of it (description, citation, etc.), or do not want your dataset to be included in this library, please get in touch through a GitHub issue. Thanks for your contribution to the ML community!


## Contact
If you have any problem about our code, feel free to contact 
- Junguang Jiang (JiangJunguang1123@outlook.com)
- Bo Fu (fb1121@qq.vip.com)
- Mingsheng Long (longmingsheng@gmail.com)

or describe your problem in Issues.

## Citation

If you use this toolbox or benchmark in you research, please cite this project. 

```latex
@misc{dalib,
  author = {Junguang Jiang, Bo Fu, Mingsheng Long},
  title = {DALIB},
  year = {2020},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/thuml/DALIB}},
}
```