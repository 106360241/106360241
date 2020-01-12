Lab3-Resample
======
 upsampling 
 --
 
   ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-3-resampling-106360241/blob/master/upsampling.png)
 
 downsampling
 --
 
  ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-3-resampling-106360241/blob/master/downsampling.PNG)
  
 lowpass filter
 --
  
  ![resample](https://github.com/DigitalSignalProcessingNTUT2018/lab-3-resampling-106360241/blob/master/LP%20filter.PNG)

*****************************************

輸出結果
--
  
 **下圖為lowpass filter 的 frequency respond**
 
 
![濾波器種類](https://github.com/DigitalSignalProcessingNTUT2018/lab-3-resampling-106360241/blob/master/LP_freqz.PNG) 


  
  
 下圖為先將10K -> 110k 在進行低通濾波 在 -> 22k 波形及頻譜圖
 --
 
 ![波形](https://github.com/DigitalSignalProcessingNTUT2018/lab-3-resampling-106360241/blob/master/110k%20to%2022k.PNG)
 

 下圖為先將10K -> 40k 在進行低通濾波 在 -> 8k 波形及頻譜圖
 --
 
 ![輸入與輸出信號頻譜](https://github.com/DigitalSignalProcessingNTUT2018/lab-3-resampling-106360241/blob/master/40k%20to%208k.PNG)
 
 
 
 
 ********************************************************
Observation
 --
 
 一開始先將以10k取樣的聲音訊號用zero-padding的方式升頻到想要的頻道，但聲音聽起來會有很多雜訊，之後透過matlab產生的低通濾波器，將一些高頻的雜訊濾除，再降回低頻，這樣聲音訊號聽起來就跟原本的差不多，不會有太多雜音出現
 
*******************************************************************************************

Source Code
--
main code 為 *resample.m*

升頻 為 *upsampling.m*

降頻 為 *downsampling.m*

低通濾波器 為 *lowpassfilter.m*

輸入訊號 為 *10khz_message.wav*
 
 

