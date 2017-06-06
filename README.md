## cbeta related materials

## 1. Metadata

https://github.com/DILA-edu/cbeta-metadata

## 2. Text

1. 带现代标点和简单标记的utf8文本

   https://github.com/mahawu/BM_u8

2. 文本处理相关程序

* https://github.com/RayCHOU/ruby-cbeta
* http://www.rubydoc.info/gems/cbeta/CBETA/P5aToText

## 3. Char Frequency

字频统计：https://github.com/DILA-edu/cbeta-metadata/tree/master/char-count

缺字文件：https://github.com/DILA-edu/cbeta-metadata/blob/master/gaiji/gaiji.json



## 4. Tripitaka Vocabulary

根据中国《通用汉字规范表》一、二级字表的制作方法，以cbeta的文本为基础语料，制作大藏经字表。

##### 步骤如下：

1. 获取前叙的cbeta文本字频统计文件char-freq.csv
2. 根据缺字文件gaiji.json，对字频文件中的缺字进行替换，替换后的文件根据是否为unicode汉字分为两个文件
   * unicode.txt
   * no_unicode.txt
3. 根据台湾异体字字典，将所有的狭义异体字替换为正字，广义异体字保留不变
4. 针对替换后的字频文件，将相同的文字进行合并，合并结果为
5. 针对合并后的文件，按照《通用汉字规范表》一、二级字表提供的算法，计算得到大藏经一二级字表。
   * 一级字表节点：4170,std,嚲,740
   * 二级字表节点：8451,std,妮,61








