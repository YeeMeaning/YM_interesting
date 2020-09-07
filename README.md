# if else 縮寫
[JS if…else…的簡短寫法](http://sodagreen.tw/wp/workblog/?p=82)

1.檢查變數並設定初始值
```js
if (!b) {
  b = 2;
}
// 簡寫
b || (b = 2);
```
2.if…else… 的情況
```js
if (a) {
  b = 1;
  c = 'nice'; 
} else {
  b = 2;
  c = 'bad';
}
// 簡寫
// `?:`為三元運算子(Ternary Operator)
a ? ( (b = 1), (c = 'nice') ) : ( (b = 2), (c = 'bad') );
```
3.單一 if 的情況
```js
if (a) {
  c = 'OK';
}
// 簡寫
// `?:`為三元運算子(Ternary Operator)
a && (c = 'OK');
a ? (c= 'OK') : '';
```
4.多個條件的情況
```js
function getA () {
  if (a === 0) {
    return 'a is zero.';
  } else if (a === 1) {
    return 'a is one.'; 
  } else {
    return 'a is not 0 nor 1.';
  }
}
// 簡寫
// `?:`為三元運算子(Ternary Operator)
function getA () {
  return (a === 0) ? 'a is zero' : (a === 1) ? 'a is one' : 'other';
}
```
# YM_interesting

如何用python 畫等高線圖

https://www.itread01.com/content/1547254807.html

劃出精美功能強大的前端表格 using DataTables
https://dotblogs.com.tw/shadow/2018/04/03/013433

複數標題用法
https://datatables.net/examples/basic_init/complex_header.html

可能的解決方案
https://stackoverflow.com/questions/51586069/error-datatable-is-not-a-function-in-electron

Electron 用以添加datatable
https://github.com/shreyamdg/electron-datatables


# CNN 計算
1. [卷積神經網路(Convolutional neural network, CNN):卷積計算中的步伐(stride)和填充(padding)](https://medium.com/@chih.sheng.huang821/%E5%8D%B7%E7%A9%8D%E7%A5%9E%E7%B6%93%E7%B6%B2%E8%B7%AF-convolutional-neural-network-cnn-%E5%8D%B7%E7%A9%8D%E8%A8%88%E7%AE%97%E4%B8%AD%E7%9A%84%E6%AD%A5%E4%BC%90-stride-%E5%92%8C%E5%A1%AB%E5%85%85-padding-94449e638e82)
![image](https://github.com/YeeMeaning/YM_interesting/blob/master/image/CNN_Tutorial_conv_layer_1.png)

2. [Convolutional Neural Networks(CNN) #2 池化層(Pooling layer)](https://www.brilliantcode.net/1586/convolutional-neural-networks-2-pooling-layer/)
![image](https://github.com/YeeMeaning/YM_interesting/blob/master/image/CNN_Tutorial_pooling_layer_1.png)
