# 修改conda虚拟环境安装路径

**问题描述：**

虚拟环境安装的路径默认放在了C盘，每个虚拟环境都很大，非常占空间。

![](https://github.com/onlyone2019/Q-A/blob/master/pictures/conda_env_install_path.png)


**解决方案一：**

`conda config --add envs_dirs newdir`

把目标路径添加进来即可。

可以使用命令 `conda config --remove envs_dirs newdir` 删除原来的路径，不过原来的路径里可能装有虚拟环境，要小心删。

**解决方案二：**

在 `C:\Users\username` 下找到文件 `.condarc` ，在后面追加：
```python
envs_dirs:
  - E://Anaconda//envs #新的环境保存位置
```

