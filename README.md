 Image Scaling
 ======
 雙線性插植法(bilinear)
 --
 這次Lab所使用的內插法為雙線性插植法(bilinear)
 想法是令f(x,y)=ax+by+cxy+d

 f(0,0)=d
 
 f(1,0)=a+d
 
 f(0,1)=b+d
 
 f(1,1)=a+b+c+d

 f(x,y)=[f(1,0)-f(0,0)]x+[f(0,1)-f(0,0)]y+[f(1,1)+f(0,0)+f(1,0)-f(0,1)]xy+f(0,0)
 
 利用上式得到的結果去進行插值
 
 這個方法相較於nearest雖然運算量較大，但縮放後得到的image品質較好
 
 不會出現像素不連續的狀況
 
 **以下為程式進行雙線性內插**
 
![雙線性插值](https://github.com/DigitalSignalProcessingNTUT2018/lab-4-image-scaling-106360241/blob/master/%E9%9B%99%E7%B7%9A%E6%80%A7%E6%8F%92%E5%80%BC.PNG) 
*******************************************************************************************
 輸入圖片
 --
![輸入圖片](https://github.com/DigitalSignalProcessingNTUT2018/lab-4-image-scaling-106360241/blob/master/6dog.jpg)

 輸出圖片
 --
`放大四倍`
![4倍大圖片](https://github.com/DigitalSignalProcessingNTUT2018/lab-4-image-scaling-106360241/blob/master/%E6%94%BE%E5%A4%A74%E5%80%8D.PNG)

`縮小九倍`

![九倍小圖片](https://github.com/DigitalSignalProcessingNTUT2018/lab-4-image-scaling-106360241/blob/master/%E7%B8%AE%E5%B0%8F9%E5%80%8D.PNG)
*******************************************************
Discussions
---
這學期因為有修數位影像處理，所以在理解影像縮放需要進行補洞的理解上比較沒問題，但課堂上是使用affine transform，來進行灰階影像的處理，而這次lab是彩色圖像，這就令我蠻苦惱的，只好用例題使用的縮放方式，再上網查一些內插法的公式進行研究，從結果發現到如果是進行放大基本上，雙線性的表現在imresize是沒有什麼區別的，但在縮小圖像上面，可以發現有一些比較不平滑的狀況出現，所以我用低通濾波器，將一些凸出的高頻濾除，雖然好了些，但相較於Imresize，自己內插後進行濾波，影像會變得稍微模糊些。 
***********************
Source code
--
source code 為 *scaling.m*
