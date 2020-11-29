* 连接服务器

  ```commonlisp
  ssh user@.....
  ```

* 创建文件

  ```
  touch filename
  ```

* 创建文件夹

  ```commonlisp
  mkdir name
  ```

* 杀死进程

  ```
  kill -9 process_id
  ```

* 本地像服务器传送文件，在本地执行

  ```
  scp /Users/zhongyuanke/data/seurat_data/spatial/allen_cortex.rds zyk@10.69.12.23:/data
  ```

* 服务器向本地传文件，在本地执行

  ```
  scp zyk@10.69.12.23:/data/file1.txt /Users/zhongyuanke/data/
  ```

* 安装r

  ```
  sudo apt-get install r-base
  ```

* 查看当前路径

  ```
  pwd
  ```

* 转到根目录

  ```
  sudo su
  ```

* 切换用户

  ```
  su name
  ```

* 把conda添加到环境变量

  ```
  vim ~/.bashrc
  echo 'export PATH="./anaconda3/bin:$PATH"'
  ```

  然后在里面添加一行 export echo 结果

  ```
  source ~/.bashrc
  ```

  

