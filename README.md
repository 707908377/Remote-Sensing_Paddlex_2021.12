# 飞浆常规赛：遥感影像地块分割 - 12月第9名方案

本项目为2021年12月参赛作品，最终得分54.29457

本项目AI Studio地址：https://aistudio.baidu.com/aistudio/projectdetail/3432894?forkThirdPart=1
欢迎小伙伴们访问，从中可以获得更加详细的介绍和可一键复现的飞桨算法代码
![image](https://user-images.githubusercontent.com/95835850/150481312-98b26be4-3a85-4b20-b930-a5023a580f95.png)

## 提交时所使用的checkpoint
最终提交结果的checkpoint使用的是/output/deeplab/路径下的best_model

## tip1
数据增强操作可以有效提升分数，对用于分割任务的数据进行操作。可以利用paddlex.seg.transforms中的Compose类将图像预处理/增强操作进行组合。

## tip2
本方案训练使用学习率为0.0001，训练轮数为35轮（Epoch1到Epoch35）

根据GPU显存设定训练时批处理图片数为8，太大容易爆显存

模型保存在output/deeplab文件下，设定为每进行一轮保存一次

## 总结与展望
可以尝试按照其他比率划分数据集

尝试丰富数据增强操作来改进

尝试从增加网络深度的角度来改进模型
