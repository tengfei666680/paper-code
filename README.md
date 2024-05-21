# 使用说明：这是《An Additive feature fusion attention based on YOLO network for aircraft skin damage detection》文章中的代码部分，是基于YOLOv7模型改进的
先按照YOLOv7模型的训练方式进行环境搭建和制作自己的数据集格式；然后即可训练模型。下图是本文提出的改进：
# 总的改进结构图：
![image](https://github.com/tengfei666680/paper-code/assets/83683292/e5665b0d-d24c-4c6c-b214-a77fcd25736d)
# 加性特征融合注意力机制结构图：
![加性特征融合注意力机制-英文](https://github.com/tengfei666680/paper-code/assets/83683292/c127282d-6dc3-4460-b536-2035d82e850b)



本文提出的加性特征融合注意力机制和动态Inner-CIOU损失函数代码分别在model/common.py中的Add_Attention类（125行）和utils/general.py/bbox_iou类/383行


模型结构的yaml文件见：cfg/training/yolov7-add_attention-1.yaml


文章中公开数据集的yaml文件见：data/VOC_2007.yaml和data/Tianchi_Aluminum_8-2_rewrite.yaml


tips：YOLOv7保存的best.pt模型的指标不是完全参考mAP0.5指标的，mAP0.5：0.95指标占比较大，本代码中还会另外保存best_map.pt文件，这是参照map0.5指标的。




