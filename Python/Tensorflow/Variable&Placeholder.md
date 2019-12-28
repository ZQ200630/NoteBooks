```python
tf.placeholder(tf.float32, [None, sizeof(vector)])  #占位符，调用时通过此喂入数据,一般为输入数据
tf.variable(tensor)  #神经网络中的变量，一般为权值或偏置
```