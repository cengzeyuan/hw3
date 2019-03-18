# 数字图像处理第三次作业
**学生姓名：曾泽源  
班级：自动化65  
学号：2160504116  
提交日期：2019/3/18**  
**摘要：**  灰度直方图是数字图像处理中最简单有用的工具。本次实验基于MATLAB软件，对附件图像进行了灰度直方图的绘制、直方图均衡化、直方图匹配、局部直方图增强和直方图阈值分割，并将结果进行分析和相应的比对，讨论处理后图像的效果和算法的适用情况。  
**关键词：**  直方图 直方图均衡化 直方图匹配 局部直方图增强 直方图阈值分割  

Project3:直方图图像增强；  
------------------

要求：  
1.把附件图像的直方图画出；   
2.把所有图像进行直方图均衡；输出均衡后的图像和源图像进行比对；分析改善内容；    
3.进一步把图像按照对源图像直方图的观察，各自自行指定不同源图像的直方图，进行直方图匹配，进行图像增强；    
4.对elain和lena图像进行7x7的局部直方图增强；    
5.利用直方图对图像elain和woman进行分割；    
  
结果讨论：    
  
1. 强度直方图以直方图形式显示不同的像素值在不同的强度值上的出现频率，对于灰度图像来说强度范围一般为[0~255]，灰度直方图一般是寻找灰度图像二值化阈值常用而且较为有效的手段之一，如果一幅灰度图像的直方图显示为两个波峰，则二值化阈值应该是这两个波峰之间的某个灰度值。    
    直方图绘制结果如下：      
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/1.jpg)  
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/1.2.jpg)    
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/1.3.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/1.4.jpg)     
    结果分析：将直方图与原始图像进行对照，我们不难发现图像的灰度分布与图像直方图之间潜在的联系：在暗图像中，直方图的分量集中分布在灰度级的低端，而亮图像的直方图分量则倾向于灰度级的高端；低对比度图像直方图所占灰度级较窄，且集中于灰度级的中部，而高对比度图像中直方图的分量覆盖了较宽的灰度级范围，同时像素分布并不均匀，没有特定的规律性。    
  
2. 直方图均衡化处理的目的是把原始图像的灰度直方图分量从比较集中的某个灰度区间变成在全部灰度范围内大致均匀分布。直方图均衡化实质是对原始图像进行非线性拉伸，进而重新分配图像像素值，使全部灰度范围内的像素数量差别不再明显。    
    均衡化后的图像及其直方图如下：    
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.1.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.2.jpg)    
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.3.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.4.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.5.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.6.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.7.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.8.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.9.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.10.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.11.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.12.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.13.jpg)     
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/2.14.jpg)     
    结果分析：首先，对比灰度直方图不难观察到直方图均衡化后图像的像素灰度分布确实更加均匀并且占据了整个灰度级范围；对比图像上可以看到，直方图均衡化后图像对比度变大，灰度色调变化范围加大。当然，也可以看到有些图像进行直方图均衡化效果并不是很好，因此，直方图均衡化并不是适用于所有的图像。    
    
3. 直方图匹配（histogram matching）是将图像直方图以标准图像的直方图为标准进行变换,使两图像的直方图相同或近似,从而使两幅图像具有类似的色调和对比度。    
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.1.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.2.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.3.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.4.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.5.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.6.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.7.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.8.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.9.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/3.10.jpg)   
    结果分析：对比源图像可以看出，大部分图像经过直方图匹配后得到了较有效的自动增强，但是依旧有少部分图像非但没有改善反而变差。因此这种自动增强的方式也不是对所有图像都适应的，还是要考虑标准图像的直方图分布和进行增强的图像自身的特点。  
    
4. 局部直方图增强不同于直方图均衡化和直方图匹配，主要针对图像的某些部分无需改动，而也存在部分需要增强效果的情况。局部直方图增强的目标为针对像素点的邻域，在邻域内进行直方图均衡化或直方图匹配，达到增强小区域中的细节的效果。  
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/4.1.jpg)  
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/4.2.jpg)  
    结果分析：可以看出，局部直方图增强令源图像的很多人物和背景细节变得非常突出，但是在部分灰度不连续部分出现了非常明显的分割，特别是elain的背景部分效果非常差。我认为是由于elain一图的背景部分较为模糊，并没有明显的细节，因此局部直方图增强的后得到的背景部分令人不适。  
    
5. 直方图分割的阈值方法是基于一定假设的。如果图像所包括的背景区域与所需分割出的目标区域大小可比，而且两者在灰度上有着明显的去表，那么这样的图像在灰度上会有明显的去表，同时其灰度直方图会呈现很明显的双峰状；其中一块峰值区域对应的是背景区域的灰度，另一块峰值区域对应的就是目标区域的灰度了。理想中的图像的灰度直方图，其背景灰度和目标灰度对应两个不同的灰度峰值，可以考虑选取位于两峰之间的峰谷值作为阈值，就能很快地将一副图像的背景与目标分割开了。但是实际中图像额灰度直方图并不都能很好的满足要求，常使用锐化等方法让图像质量尽量满足要求。  
这是采用的是Otsu阈值分割处理图像。  
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/5.1.jpg)   
![](https://github.com/cengzeyuan/hw3/blob/master/2160504116/5.2.jpg)   
    结果分析：可以看到，分割后的图像都很好地从原图的背景中脱离出来，但是原本灰度较大的部分（如双手、脸部、袖口处的衣物等）被认为是背景而被删除。可以看出，直方图分割对于目标部分区域与背景区域灰度值相近或者更低时，会出现一定的错误删除，对最终的结果会有一定的影响。  
    
##  附录    

【参考文献】  

[1] Gonzalez R , Woods R , Eddins S . 数字图像处理:MATLAB版[M]. 电子工业出版社, 2005.    

[2] 周品.MATLAB数字图像处理 北京：清华大学出版社，2012  

[3] 杨杰.数字图像处理及MATLAB实现 北京：电子工业出版社，2010  
