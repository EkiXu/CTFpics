# CTF pics

```
用于检测常见隐写工具实现的图片隐写。
支持二次开发，欢迎各位dalao们来交流和pull 
联系方式：2297571095@qq.com
```

### 前置环境

kali/ubuntu python3 

需要python中的

```
stegpy 库（暂未用到）
```

apt install steghide

```
zsteg环境 （自行安装）
outguess 的环境（已经打包在整个工具里）
```

-------

### 用法

python3 ctf.py 回车后

等待出现input the pic name

输入pic name 

剩下的按照指示进行即可。

### 功能

主要检测利用stegdetect以及png中的常见隐写方式

jpg为主要检测对象

进行了stegdetect 以及由于其不准确性。测量出的算法不准确，于是使用了全部的已知图片隐写算法进行测试，和弱密码爆破测试。

经测试steghide jphide outguess 功能均无问题。

png以及其他方面的图片暂为进行更高级的扩展。

后期加入crc自动校验，webp，bmp，以及盲水印等功能检测。

也希望dalao来帮忙pull

----------

若有任何问题请联系：QQ：2297571095

----------------------

2021.2.5 

## 加入了功能

png的带密钥lsb隐写。

其中有两种模式

第一种是基于有密码的简单破解。

需要自行下载环境

```
python2 
pip2 install Crypto
```

第二种依然是我们的爆破模式

若发现爆破出的data并非我们想要/乱码

会出现input anything to continue .

如果不想爆破了直接ctrl C 就可以了

------------------

我加了lsbtest.png 大家可以自行尝试。

最近期望加入的功能，希望有大佬一起来研究:

1. 盲水印（主要DCT）
2. 其他格式图像的隐写 （GIF，bmp，webp）
3. 基于图片像素的检测以及简单操作。