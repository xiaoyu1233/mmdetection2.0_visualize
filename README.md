# mmdetection2.0_visualize
It is a simple tool based on mmdetection2.0. The tool is used for visualize test result produced by mmdetection 2.0, including drawing PR curves and loss curves.（PR曲线绘制，loss曲线绘制）

# What can It do
The program supports drawing two figures. The loss figure includes six kinds of training loss. The PR figure includes PR curve and F1-score.

loss figure:

1. loss_rpn_bbox

2. loss_rpn_cls

3. loss_bbox

4. loss_cls

5. loss

6. acc

PR figure

1. PR_curve

2. F-measure

# installation

1. Git Clone

```Python
git clone https://github.com/xiaoyu1233/mmdetection2.0_visualize
```

2. Put File in the Proper Position

put `visualize.py` under `/mmdetection/tools/`

put `voc_eval_visualize.py` under `/mmdetection/tools/`

put `mean_ap_visualize.py` under `mmdetection/mmdet/core/evaluation/`

# How to Use

1. Loss figure

When training finished, you will have work _dirs directory in your mmdetection directory.
Find your latest json directory and copy the path. And use it in this command.

At the same time, you should prepare a directory in your mmdetection diretory.
Create output/work_dirs/faster_rcnn_r50_fpn_1x_voc directory.(The diretory in your output folder should be same as your work_dirs, or you can change it in code by yourself).
```
python tools/visualize.py work_dirs/faster_rcnn/faster_rcnn_r50_fpn_1x_voc/xxxxxxxx.log.json(your latest path)
```
Then check the output/work_dirs/faster_rcnn_r50_fpn_1x_voc directory, you will get the loss figure.

2. PR figure 

Make sure voc_eval_visualize.py and mean_ap_visualize.py settled down
And prepare a directory in your mmdetection diretory.
Create mmdetection in your mmdetection directory.
Use this command
```
python tools/voc_eval_visualize.py ./result.pkl(your pkl file path) ./configs/faster_rcnn/faster_rcnn_r50_fpn_1x_voc.py(your config file)
```
Then check mmdetection/mmdetection directory, you will get PR figure.

# Result

![](https://github.com/xiaoyu1233/mmdetection2.0_visualize/raw/main/example/20201124_194853.log.json_result.png)

![](https://github.com/xiaoyu1233/mmdetection2.0_visualize/raw/main/example/r50_voc_PR_Curve_each_class.png)

# Appendix

if issues are not solved in time, welcome to talk with me at my CSDN blog: https://blog.csdn.net/AI414010






