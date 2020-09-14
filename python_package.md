# python创建包流程

假设包的名字叫 testp

* 在testp文件夹同级目录下创建文件setup.py

  内容大致如下：

  ```python
  from distutils.core import setup
  from setuptools import setup, find_packages
  
  setup(
      name='test',
      version='0.0.1',
      keywords=('integration', 'single cell'),
      description='',
      license='MIT License',
      url='https://github.com/drizzlezyk/test',
      author='Yuanke Zhong',
      author_email='yuanke.zhong@nwpu-...com',
      packages=find_packages(),
      platforms='any',
  )
  ```

* 在test文件夹第一层创建\__init__.py，里面可以不用写内容

* 在test里每一个子文件夹创建\__init__.py，这样可以保证每个文件都能调用、

* 在命令行转到该文件夹所在目录，然后输入，这一步结束可以看到test同级目录下有build文件夹

  ```
  python3 setup.py build
  ```

这样在该路径下直接运行 

```
pip install .
```

就可以在本地安装这个包



## 上传到pypi

* 执行如下命令

  ```
  python3 setup.py sdist
  ```

* 在test 同级目录下sdist下会生成一个压缩包

* 执行如下：

  ```bash
  python setup.py upload
  ```

