# 其它参考
> [one-python：三千Lib 库，每领域取Top 1](https://github.com/vinta/awesome-python)
# 核心库和统计
1. **Numpy**
```
NumPy用于处理大型多维数组和矩阵，并通过大量的高级数学函数和实现方法进行各种操作。

```

2. **Scipy**
```
  SciPy基于NumPy，因此扩展了NumPy的功能。
  SciPy的主要数据结构是由Numpy实现的多维数组。当中包括许多解决线性代数、概率论、积分等任务的工具。

```

3. **Pandas**
```
  Pandas是一个Python库，提供高级数据结构和各种分析工具。主要特点是能够将相当复杂的数据操作转换为一两条命令。Pandas包含许多用于分组、过滤和组合数据的内置方法，以及时间序列功能。

```
4. **Sympy**
```
科学计算库，用一套强大的符号计算体系完成诸如多项式求值、求极限、解方程、求积分、微分方程、级数展开、矩阵运算等等计算问题。
```
# 可视化
1. **Matplotlib**
```
创建二维图表和图形的低级库。使用Matplotlib，你可以构建直方图、散点图、非笛卡尔坐标图等图表。

```

2. **Seaborn**
```
Seaborn是基于matplotlib库更高级别的API。它包含更适合处理图表的默认设置。此外，还包括时间序列等丰富的可视化图库。

```

3. **Bokeh**
```
侧重于交互可视化，Bokeh库使用JavaScript小部件，在浏览器中创建交互式和可缩放的可视化。Bokeh提供了多种图形集合、样式，并通过链接图、添加小部件和定义回调等形式增强互动性。

```
   
4. **Plotly**
```
基于Web用于构建可视化工具箱Plotly能够让你轻松构建复杂的图形。Plotly适用于交互式Web应用程序。可视化方面包括等高线图、三元图和三维图。

```
5. **Pydot**
```
Pydot用于生成复杂的定向图和非定向图。它是用Python编写的Graphviz接口。使用Pydot能够显示图形结构，这经常用于构建神经网络和基于决策树的算法。

```
# 数据挖掘
1. **Statsmodels**
```
使用统计模型的估算方法进行数据挖掘

```

# 机器学习
1. **SciKit-Learn**
```
Scikit-learn基于NumPy和SciPy，并且是处理数据方面的不错选择。Scikit-learn为许多机器学习和数据挖掘任务提供算法，比如聚类、回归、分类、降维和模型选择。

```
2. **XGBoost / LightGBM / CatBoost**
```
梯度提升(gradient boosting)是最流行的机器学习算法之一，这在决策树模型中是至关重要的。

```
3. **Eli5**
```
通常机器学习模型预测的结果并不特别清晰，这时就需要用到eli5了。它可以用于可视化和调试机器学习模型，并逐步跟踪算法运行情况。同时eli5能为scikit-learn，XGBoost，LightGBM，lightning和sklearn-crfsuite库提供支持。

```
# 深度学习
1. **Keras**
```
使用Theano或TensorFlow作为后端，微软正努力整合CNTK作为新的后端

```
2. **TensorFlow**
```
TensorFlow能够用于多个数据集的人工神经网络。TensorFlow的主要应用包括对象识别、语音识别等等。
```
3. **PyTorch**
```
PyTorch是一个大型框架，能通过GPU加速执行tensor计算，创建动态计算图并自动计算梯度。此外，PyTorch为解决神经网络相关的应用提供了丰富的API。
PyTorch基于Torch，它是用C语言实现的开源的深度学习库。

```
4. **caffe**
```
Deep learning framework made with expression, speed, and modularity in mind.

```

# 分布式深度学习
1. Dist-keras / elephas / spark-deep-learning
```
由于越来越多的用例需要大量的精力和时间，深度学习问题变得更为重要。但是，使用Apache Spark之类的分布式计算系统能够更容易处理大量数据，这又扩展了深度学习的可能性。

```
# 自然语言处理
1. **NLTK**
```
NLTK是一组库，是进行自然语言处理的平台。在NLTK的帮助下，你可以通过多种方式处理和分析文本，对其进行标记和提取信息。NLTK还可用于原型设计和构建研究系统。

```
2. **SpaCy**
```
SpaCy是自然语言处理库，具有出色的示例、API文档和演示应用。该库用Cython编写，Cython是C语言在Python的扩展。它支持将近30种语言，提供简单的深度学习集成，并能确保稳定性和高准确性。SpaCy的另一个强大功能是无需将文档分解，整体处理整个文档。

```
3. **Gensim**
```
用于语义分析、主题建模和矢量空间建模，建立在Numpy和Scipy之上。可用于检测重复模式文本。

```
# 数据抓取
1. **Scrapy**
```
爬虫框架，可用于创建扫描页面和收集结构化数据。
```
# **HTTP Request**
1. **[requests](https://github.com/kennethreitz/requests)**
# Web Content Extracting
1. **[newspaper](https://github.com/codelucas/newspaper)**
# Web框架
1. **Django**
```
The most popular full featured web framework in Python
```
# Markdown parser
1. **mistune** 
```
The fastest markdown parser in pure Python with renderer features, inspired by marked.

```
# Optical Character Recognition (OCR)

1. **pytesseract **
A wrapper for Google Tesseract OCR.
# Chinese Word Segmentation
1. **jieba** 
Chinese Words Segmentation Utilities.
# Concurrency and Networking
1. **gevent**
A coroutine-based Python networking library that uses greenlet.


