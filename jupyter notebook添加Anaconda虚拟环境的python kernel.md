### jupyter notebook添加python kernel

1. 在C:\Users\yinzm\AppData\Roaming\jupyter\kernels\下面创建一个文件夹，这个文件夹最好使用虚拟环境的名字，便于识别。
2. 然后在该文件夹下创建一个kernel.json文件，文件内容如下：
>
    {
     "language": "python",
     "display_name": "rqalpha",
     "argv": [
      "D:\\Anaconda3\\envs\\rqalpha\\python.exe",
      "-m",
      "ipykernel_launcher",
      "-f",
      "{connection_file}"
     ]
    }
    保存，重启jupyter notebook。

    
3. 重新启动之后发现确实多了一个为rqalpha的kernel，但是却始终启动不了这个kernel。后来发现是缺少ipykernel。于是利用如下命令安装：
>
    conda install -n rqalpha ipykernel
    至此，问题得到解决。

如果经常需要用jupyter notebook，那么最好在创建虚拟环境的时候便安装好ipykernel，命令如下：

conda create -n rqalpha python=3.5 ipykernel
