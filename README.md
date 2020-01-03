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
這學期因為有修數位影像處裡, 所以在理解影像縮放需要進行補洞的理解上比較沒問題
