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

1. 获取前叙的cbeta文本字频统计文件char-freq.csv。
2. 根据缺字文件gaiji.json，对字频文件中的缺字进行替换，替换后的文件根据是否为unicode汉字分为两个文件。
   * unicode.txt。文件中no_gaiji表示缺字文件中无此字，其余类型参照缺字文件。
   * no_unicode.txt。
3. 根据台湾异体字字典，判断unicode.txt中的异体字类型，结果为unicode_types.txt。（std表示正字，single_vt表示狭义异体字，mul_vt表示广义异体字。）
4. 查询台湾异体字字典，获取unicode_types.txt中的狭义和广义异体字对应的正字，得到文件variants.txt。
5. 根据variants.txt，将unicode.txt中所有的狭义异体字替换为正字，广义异体字则保留不变。
6. 针对替换后的字频文件，将相同的文字进行合并，合并结果为final_char_freq.txt和detail_final_char_freq.txt。其中，detail_final_char_freq.txt记录了合并之前的字频。
7. 针对合并后的文件，按照《通用汉字规范表》一、二级字表提供的算法，计算得到大藏经一二级字表。
   * 一级字表节点:8632,渕,36
   * 二级字表节点:4176,魍,657








