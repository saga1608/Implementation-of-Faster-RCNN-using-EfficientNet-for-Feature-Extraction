# IMPLEMENTATION OF FASTER RCNN

### Faster R-CNN can be generally divided into two parts, RPN part and R-CNN part, each part is an independent neural network and can be trained jointly or separately.

Step by step implementation:
1.	Features Extraction from the image using efficient net.
2.	Creating anchor targets.
3.	Locations and objectness score prediction from the RPN network.
4.	Taking the top N locations and their objectness scores aka proposal layer
5.	Passing these top N locations through Fast R-CNN network and generating locations and cls predictions for each location is suggested in 4.
6.	generating proposal targets for each location suggested in 4
7.	Using 2 and 3 to calculate rpn_cls_loss and rpn_reg_loss.
8.	using 5 and 6 to calculate roi_cls_loss and roi_reg_loss.

