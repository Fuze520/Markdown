### pip 使用国内镜像源

#### 1. 命令行模式

当我们使用`pip`或`pip3`去安装第三方库的时候，会遇到下载安装速度**很慢**的情况。
```python
pip3 install package-name
```
这是因为在默认情况下，`pip`或`pip3`使用的是国外的镜像`https://pypi.org/simple `，所以下载的速度会非常慢甚至无法下载。

因此，我们可以使用国内的镜像源来进行第三方库的下载安装，从而解决下载慢或无法下载的问题。即在使用`pip`或`pip3`命令的时候，**添加`-i`参数来指定镜像地址**，例如下方的命令使用的是清华大学镜像源（也可使用其他镜像源）：
```python
pip3 install package-name -i https://pypi.tuna.tsinghua.edu.en/simple
```

---

##### 常用的国内镜像源
| 国内镜像源 | 地址 |
| --- | --- |
| 清华大学 | https://pypi.tuna.tsinghua.edu.cn/simple |
| 阿里云 | http://mirrors.aliyun.com/pypi/simple |
| 中国科学技术大学 | https://pypi.mirrors.ustc.edu.cn/simple |
| 豆瓣 | https://pypi.douban.com/simple |

---

#### 2. 添加配置文件
当然也可以通过设置`～/.pip/pip.conf`文件来永久设置镜像源(以清华大学镜像源为例)。如果没有就需要先手动创建`.pip`文件夹（**文件夹前面有一个`.`表示该文件夹为隐藏文件夹**）。
```txt
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple

[install]
trusted-host = pypi.tuna.tsinghua.edu.cn
```
设置完之后，在`terminal`中可以查看配置后使用的镜像源：
```shell
pip3 config list   
global.index-url='https://pypi.tuna.tsinghua.edu.cn/simple'
install.trusted-host='https://pypi.tuna.tsinghua.edu.cn'
```
**当然**，我们也可以同时配置多个镜像源，这样在使用`pip`的时候就会按照`index-url`的顺序去尝试。
```txt
[global]
index-url=https://pypi.tuna.tsinghua.edu.cn/simple
extra-index-url=http://mirrors.aliyun.com/pypi/simple
extra-index-url=https://pypi.mirrors.ustc.edu.cn/simple
extra-index-url=https://pypi.douban.com/simple

[install]
trusted-host = pypi.tuna.tsinghua.edu.cn
trusted-host = mirrors.aliyun.com
trusted-host = pypi.mirrors.ustc.edu.cn
trusted-host = pypi.douban.com
```