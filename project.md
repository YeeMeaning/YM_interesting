# Pinhole camera model 

What Is Camera Calibration? [Mathwork](https://www.mathworks.com/help/vision/ug/camera-calibration.html)
針孔相機模型 Pinhole Camera Model [Math.py](https://allen108108.github.io/blog/2020/02/06/%E9%87%9D%E5%AD%94%E7%9B%B8%E6%A9%9F%E6%A8%A1%E5%9E%8B%20%20Pinhole%20Camera%20Model/)



# 相機學習

鏡頭基礎
焦距、視角與透視[SONY](https://www.sony.com.tw/zh/electronics/focal-length-angle-of-view-perspective)

鏡頭規格
![image](https://github.com/YeeMeaning/YM_interesting/blob/master/image/%E5%90%84%E5%BB%A0%E7%89%8C%E9%8F%A1%E9%A0%AD%E8%A6%8F%E6%A0%BC.png)

## 鏡頭視角 簡易計算公式 [Ref](http://www.kyyeung.com/Photo/060525/060525.htm)

![image](https://github.com/YeeMeaning/YM_interesting/blob/master/image/Camera%20FoV.png)

鏡頭視角是以覆蓋底片對角線為直徑的圓來計算的，以135相機來說，根據勾股定理，底片對角線約為43.2666mm。<br>
<br>

設： A = 鏡頭視角 / 2 ， b = 焦距 ， a = 底片對角線 / 2<br>
則： 鏡頭視角 = 2A = 2 * 反正切 ((底片對角線 / 2) / 焦距 ) = 2 * tan-1 (( a / b )<br>
例：50mm鏡頭的視角 = 2 * tan-1 (( 43.2666 / 2 ) / 50 ) = 47 度<br>
<br>
以上的公式可以應用在實際拍攝中，例如不只一次有人問類似這樣的問題：假如用等效焦距為75mm的鏡頭豎拍身高1.7米的全身人像(滿畫面)，應該距離目標多遠呢。<br>
假如我們知道鏡頭的視角，當然可以計算出相應的物距。但我找到一個更簡單的方法，根據上面的正切公式我們可以推導出以下公式：(以正常拍攝情況下，焦距約等於像距計算)<br>
影像大小 / 焦距 = 實物大小 / 物距<br>
即： a / b = a1 / b1  <br>
演化為： 物距 = 焦距 * 實物大小 / 影像大小<br>
即： b1 = b * a1 / a<br>
以上面的例子套入這個公式即：<br>
所需拍攝距離約為  75 * 1.7 / 36 = 3.54米<br>
<br>
<br>
## 鏡頭視角：鏡頭中心點到成像平面對角線兩端所形成的夾角就是鏡頭視角。<br>
OpenGL視角視線與顯示的垂直方向所成的角度。[來源](https://codertw.com/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80/562893/)<br>

以135片幅規格，部分焦距的視角：<br>
　　　　　　　　焦長(mm)　　視角(度）<br>
　　　　　　　　12.00　　　121.9657188<br>
　　　　　　　　14.00　　　114.1821314<br>
　　　　　　　　15.00　　　110.5270374<br>
　　　　　　　　18.00　　　100.4756817<br>
　　　　　　　　20.00　　　94.49321352<br>
　　　　　　　　21.00　　　91.70210518<br>
　　　　　　　　25.00　　　81.74138908<br>
　　　　　　　　28.00　　　75.38064962<br>
　　　　　　　　30.00　　　71.59151983<br>
　　　　　　　　31.00　　　69.81841782<br>
　　　　　　　　35.00　　　63.4399666<br>
　　　　　　　　40.00　　　56.81194376<br>
　　　　　　　　43.00　　　53.41395316<br>
　　　　　　　　45.00　　　51.35092643<br>
　　　　　　　　50.00　　　46.79300334<br>
　　　　　　　　55.00　　　42.94269031<br>
　　　　　　　　58.00　　　40.90982996<br>
　　　　　　　　60.00　　　39.65405731<br>
　　　　　　　　70.00　　　34.34724073<br>
　　　　　　　　77.00　　　31.38563313<br>
　　　　　　　　80.00　　　30.26361357<br>
　　　　　　　　85.00　　　28.55832225<br>
　　　　　　　　90.00　　　27.03156212<br>
　　　　　　　　100.00　　 24.41373028<br>
　　　　　　　　135.00　　 18.20811949<br>
　　　　　　　　180.00　　 13.70644967<br>
　　　　　　　　200.00　　 12.3469684<br>
　　　　　　　　300.00　　 8.24903628<br>
　　　　　　　　400.00　　 6.191454161<br>
　　　　　　　　500.00　　 4.954898587<br>
注:   （１）135 片幅：大小為 36*24mm：等效即為標示。<br>
　　　　　Canon: 1Ds、5D系列；<br>
　　　　　Nikon: D3、D700；<br>
　　　　　Sony: A900。<br><br>
　　（２）APS-H 片幅：大小為 27*18mm：等效焦距*1.3。<br>
　　　　　Canon: 1D系列；<br>
　　　　　Leica: M8。<br><br>
　　（３）APS-C 片幅：大小為 23.6*15.8mm：等效焦距*1.5。<br>
　　　　　Nikon: D300、D90、D60；<br>
　　　　　Pentax: K20D、K200D、K-m；<br>
　　　　　Sony: A700、A350<br>
　　　　　APS-C 片幅：大小為 22.8*14.8mm：等效焦距*1.6。<br>
　　　　　Canon: 40D、450D、1000D。<br>
　　　　　Sigma 片幅：大小為 20.7*13.8mm：等效焦距*1.7。<br>
　　　　　Sigma: SD14、DP1。<br><br>
　　（４）4/3 片幅：大小為 18*13.5mm：等效焦距*2。<br>
　　　　　Leica: Digilux 3；<br>
　　　　　Olympus: E-3、E-520、E-420；<br>
　　　　　Panasonic: G1、L10。<br><br>

鏡頭有各自固有的焦距，焦距不同拍攝範圍也相應地有很大變化。變焦鏡頭也是同樣，當變焦到一定焦距時的固定視角與該焦距定焦鏡頭是相同的。下面將說明鏡頭所具有的焦距與視角的關係，同時學習因視角變化所導致的照片效果變化。


