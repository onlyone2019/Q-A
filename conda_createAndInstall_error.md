# conda 不能创建环境 不能下载东西

每次报错基本都有这两句话：
```python
json.decoder.JSONDecodeError: Unterminated string starting at: line 78753 column 5 (char 2031407)
$ D:\***\conda-script.py create -n py37 python=3.7
```

应该是实验室网络的问题，网络极慢而且不稳定，应该是之前update repo信息时网络有问题出现了污染。

**解决方案：**

`conda clean -i`

[参考](https://www.jianshu.com/p/2bca744fcd82)