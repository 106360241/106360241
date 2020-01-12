Graphic Equalizer
======
Purpose
--

透過調整各通道的增益，經過濾波以後，將每個通道的結果加起來，就可以得到各種不同聲音效果
*****************************************************************************************
frequency response
--

lowpass f from 0 to 1000
 --
 
   ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-5-graphic-equalizer-106360241/blob/master/lowpass.PNG)
 
 bandpass f from 1000 to 2000
 --
 
  ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-5-graphic-equalizer-106360241/blob/master/bandpass1.PNG)

bandpass f from 2000 to 3000
 --
 
  ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-5-graphic-equalizer-106360241/blob/master/bandpass2.PNG)
  
 highpass f over 3000
 --
  
  ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-5-graphic-equalizer-106360241/blob/master/highpass.PNG)

*****************************************
filter design
--

  ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-5-graphic-equalizer-106360241/blob/master/%E6%BF%BE%E6%B3%A2%E5%99%A8%E8%A8%AD%E8%A8%88.PNG)

輸入訊號經過各通道的頻譜圖(最後為各通道加起來的輸出結果)
--

  ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-5-graphic-equalizer-106360241/blob/master/%E9%A0%BB%E8%AD%9C%E5%9C%96.PNG)
  
 各通道的增益設定
 --
 
  ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-5-graphic-equalizer-106360241/blob/master/%E5%80%8B%E9%80%9A%E9%81%93%E5%A2%9E%E7%9B%8A.PNG)
  

 
*******************************************************************************************

Source Code
--

main code 為 *equalizer.m*

濾波器 為 *myfilter.m*

輸入訊號 為 *song-8k.wav*

輸入訊號經過各通道後乘上各自的增益加起來的輸出訊號 為 *out_song.wav*
 


