# 产品需求文档

|发布日期|1/12/2018|
| ---------- | --- |
|史诗名称|悦读小程序|
|文件现状|进行中|
|文件的主人|周昱瑾|
|领头的设计师|周昱瑾|
|领头的开发者|周昱瑾|

> #### [PRD部分]
- #### [加值宣言](#chapter1)
- #### [核心价值](#chapter2)
- #### [用户痛点宣言](#chapter3)
- #### [人工智能概率性与用户痛点](#chapter4)
- #### [需求列表与人工智能API加值](#chapter5)

> #### [原型部分]
- #### [交互及界面设计](#chapter6)
- #### [信息设计](#chapter7)
- #### [原型文档](#chapter8)

> #### [API 产品使用关键AI或机器学习之API的输出入展示部分]
- #### [使用水平](#chapter9)
- #### [使用比较分析](#chapter10)
- #### [使用后风险报告](#chapter11)



## 一、产品介绍
- 本产品文档中出现的专业术语说明

|名词|说明|
| ---------- | --- | 
|[OCR技术](https://baike.baidu.com/item/OCR%E6%8A%80%E6%9C%AF/15695472?fr=aladdin)|OCR技术是通过扫描等光学输入方式将各种票据、报刊、书籍、文稿及其它印刷品的文字转化为图像信息，再利用文字识别技术将图像信息转化为可以使用的计算机输入技术。|
|深度学习|作为机器学习的新领域，其动机在于建立、模拟人脑进行分析学习的神经网络，它模仿人脑的机制来解释数据，例如图像，声音和文本。|
|[NLP](https://baike.baidu.com/item/nlp/1515237)|自然语言处理技术，可以支持文本关键词提取及字词检索等功能|
|NMT|神经网络机器翻译，也是当前效果最好的翻译模式|

<h3 id="chapter3">（二）产品背景（用户痛点宣言）</h3>
时代发展，互联网逐渐改变人们的阅读方式，电子书已经逐渐普及，但是纸质版书籍在人们学习生活中仍处于不可替代的地位。阅读纸质版书籍的过程中，人们难免会有想要摘录、寻找关键内容或翻译段落等一系列的需求，在这种情况下，手抄笔记，一行一行寻找关键词，利用有道云等查询单词翻译的操作会大大浪费读者的时间。除此以外，在很多时候，我们利用网络搜集资料的过程中会遇到无法复制或下载的情况，需要登录不同的网站，充值来提高搜索资料的效率，过程繁复，手打资料又十分浪费时间。基于以上，故希望能够开发出一个集识别，编辑，翻译以及检索功能为一体的悦读小程序，提高学习效率。
<h3 id="chapter1">（二）产品市场（加值宣言）</h3>
经过调查，可发现目前已有很多产品运用ocr技术来进行图片文字识别提取，例如"全能扫描王","文字提取小程序"等，事实证明简单的图片文字提取已经不是难事，但是市面上这几款应用都不可以识别繁体字和图片中的logo等等，技术仅限于简单文本，同时识别之后不可以进行字词检索标记。基于现状，现将采用百度的OCR识别API加上NLP中的文字提取技术对现有产品进行加值和优化。
<h3 id="chapter2">（二）产品概述（核心价值）</h3>
悦读小程序以文字提取为基础功能，用户可以通过拍照或上传图片的方式来快速获取可编辑的文字信息，加值功能为字词检索计数，辅助功能为文本翻译，文本复制等。
<h3 id="chapter4">（二）产品使用场景设想（人工智能概率性与用户痛点）</h3>
- OCR文字识别技术：百度api给予深度学习技术及最优算法，整体精确度＞90%，并提供高精度版。
- NLP关键词提取技术：在文本提取精确度＞90%的基础下，分词精确度＞99%
- 谷歌研究表明，NMT目前最高的准确率可＞87%

|场景|方式|可行概率性|
| ---------- | --- | --- | 
|日常会议或课堂中|用手机拍下PPT、演示稿，能立即对图片中的文字进行编辑，而不再因为慌于抄写而错过了台上的精彩分享|＞90%|
|超市里|随手拍下想买的商品分享给家人，即时从图片中提取文字而不用拉动图片放大看文字，快速解决“选择困难症”|＞70%
|编辑室内|随手拍海量纸质资料进行图片文字提取编辑，以便排版、存档、检索，传统媒体数字化转型无需再消耗巨大人力在前期资料归集上|＞90%
|家里|长辈为拉近与儿孙辈的距离，不用再对着年轻人发来的图片一筹莫展，通过图片文字提取识别便能够看清图上文字|＞60%
|快递行业内|帮助工作人员快速识别字迹潦草的字体，提高工作效率|＞80%
|搜集资料时|帮助用户快速提取无法复制或者下载的文档，提高工作或学习效率|＞95%
|遇到不同语种时|帮助快速翻译和提取文本，减少语言障碍|＞90%|
|遇到生僻字无法输入时|快速提取可编辑文字供用户使用|＞95%|



## 二、产品目标
- 悦读小程序能够借助百度的 OCR API 人工智能技术进行网络识别,将图片中的文字快速转换为可编辑的文字供用户使用。
- 同时小程序中的字词检索功能，可以对图片中的文字进行关键词搜索，快速定位到相应位置，并可对字词进行计数，统计其出现的次数。
- 除了最基本的文字识别提取之外，小程序中会加入语言翻译功能，用户可根据自我需求设置想要的识别语言。

<h2 id="chapter5">三、需求分析（需求列表与人工智能API加值）</h2>

|#|功能|用户案例|重要程度|技术领域|
| ---------- | --- | --- | --- |--- |
|1.|文字提取|阅读纸质版书籍或是图片中文字无法获取又不想手打的时候|重要|OCR|
|2.|提取关键字|用户想要快速定位到某个特定的词|重要|NLP|
|3.|文本翻译|用户想要识别时自动转换为需要的语言，节省手打搜索时间|次重要|NMT/百度拍照翻译sdk|

### 可用API
- 百度OCR文字识别api
- 阿里云关键词提取api


><h2 id="chapter9"> 四、可行性展示（API 产品使用关键AI或机器学习之API的输出入展示 ）</h2>

### （一）[以调用百度OCR api为例](http://ai.baidu.com/tech/ocr/general)

###### 1. 提取整段文字
- 输入：整段图片文字
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/1.png)
- 输出：可编辑的整段英文
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/2.png)

###### 2.提取图片中的logo文字
- 输入：场景图片
- ![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/4.png)
- 输出：logo文字
- ![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/5.png)

###### 3.生僻字提取
- 输入：不认识的生僻字
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/21.png)
- 输出：可编辑的生僻字
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/22.png)

### （二）[代码尝试](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/test.ipynb)
- 读取图片——奖状
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/jz.jpg)
- 运行代码
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/dm.png)
- 读取结果
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/dm1.png)

<h3 id="chapter10">（三）API使用比较分析</h3>

- 搜狗 OCR API：这个接口识别效果很好，速度、准确率都没的说！但其对于图片的尺寸有规定，较小的文字无法识别
- 百度 OCR API：其识别的精确度很好，但是标点符号识别不太准确，速度一般，可以接受，但不如搜狗 OCR API。
- 腾讯 OCR API：同样比较准确的，但速度比较慢。
- 有道 OCR API：速度很快，平均 0.3-0.4 秒就可识别出来，但是接口有 IP 请求的限制，一段时间内识别次数太多就不行了。
总结：综上比较，从识别速度，识别准确度以及识别次数等方面综合考量，选择使用百度OCR API。

<h3 id="chapter11">（四）API使用风险评估</h3>

#### 问题：图中文字识别不全
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/23.jpg)
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/23.png)
- 总结：目前的ocr文字提取技术对于图片的质量有一定的要求，正面照方能保证识别准确度，对于光照或角度影响导致的文字无法完全识别是眼下解决的难题，在很多时候人们拍照的时候很难保证照片的清晰度，这就给识别准确性带来挑战性，一定程度上会影响用户的体验感。

#### 解决方式：图片预处理环节
基于图片清晰度的影响，这里提出图片预处理的3个办法，若嵌入小程序中，或可减少识别失误率。
1. 图片灰度化
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/30.png)
2. 图片二值化
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/31.png)
3. 平滑中值去噪
- ![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/32.png)

## 原型部分

><h3 id="chapter7">信息设计</h3>

## 五、产品结构图
### 产品功能结构图
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/jgt.png)
### 产品信息结构图
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/xxjgt.png)
## 六、产品流程图
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/lct1.png)
## 七、全局说明

><h3 id="chapter6">交互及界面设计</h3>

### （一）授权登录页面
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/before.png)
### （二）主页交互
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/11.png)
### （三）拍照交互
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/12.png)
### （四）导入图片交互
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/13.png)
### （三）编辑交互
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/15.png)
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/14.png)
![](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/images/16.png)
><h3 id="chapter8">原型文档</h3>
- [完整的原型文档](https://zhou-yu-jin.github.io/final/#g=1&p=%E4%BA%A4%E4%BA%92%E9%80%BB%E8%BE%91%E9%A1%B5)
- [核心功能视频展示](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/1.mp4)
## 不做（超范围功能）
根据识别文字，告诉读者文本出自于哪里，在哪些地方应用过，并推荐相关知识领域的书籍
- [PRD_B](https://github.com/Zhou-Yu-Jin/API_ML_AI/blob/master/PRD_B.md)
