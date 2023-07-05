```python
LUConv模块
先进行3D的卷积nn.Conv3D再正则化BatchNorm3D后经过激活函数nn.ELU() else PReLU
```

```python
_make_nConv 模块
由depth个LUConv模块组成的深层网络层 装在列表中，即返回的是列表
```

```python
InputTransition 模块
将输入转为16个通道+平铺输入

先进行一个3D卷积nn.Conv3D，获取重复值比例，进行正则化BatchNorm3D，然后，x根据重复值比例重复值，返回进过一次3D卷积nn.Conv3D的out和经过激活函数的x
```

```
DownTransition 模块

```

