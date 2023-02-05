## pip search
对于一些常用的Python库来说，例如Pandas，Numpy等，我们能立马反应过来用
```Python3
python3 -m pip install pandas
```
来安装依赖库，但是如果我们遇到一些不常用的依赖库、或者是安装后显示如下错误的依赖库时，
```
ERROR: Could not find a version that satisfies the requirement smtplib (from versions: none)
ERROR: No matching distribution found for smtplib
```
我们可以使用
```Python3
python3 -m pip search xxx
```
来寻找依赖库的归属，然后做后续的安装与使用。**但是**，目前PyPI已经不再支持上述搜索指令，在执行该命令时，会报如下错误：
```
ERROR: XMLRPC request failed [code: -32500]
RuntimeError: PyPI no longer supports 'pip search' (or XML-RPC search). Please use https://pypi.org/search (via a browser) instead. See https://warehouse.pypa.io/api-reference/xml-rpc.html#deprecated-methods for more information.
```
所以，我们需要移步到`https://pypi.org/`网站来进行搜索操作。
