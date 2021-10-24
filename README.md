# BCCD Dataset  
적혈구 백혈구 혈소판 Detection  
This is an implementation of Faster RCNN on BCCD image set. The data set contains of roughly around 400 microscopic images of blood along with xml files containing the annotations and information about bounding boxes. We have to identify and localize, in an image, whether a cell is RBC, WBC or Platelet. I used Tensorflow object detection api for this. You can find the dataset here https://github.com/Shenggan/BCCD_Dataset  

![1](https://user-images.githubusercontent.com/55770741/138584321-26dc1efc-22ca-4287-88c7-acf4d37929ef.JPG)<br><br>

# Review  
Yolov5와 faster rcnn 활용해서 BCCD Dataset을 train validation해보았다. Yolov5에서는 BCCD Dataset을 coco로 바꾼 뒤 Yolo Dataset으로 변경하여 train에 적용하였다
faster rcnn에서는 mmdetection tools을 사용하여 진행하였는데,  coco로 바꾼 뒤 mmcv config을 설정하여 train을 진행하였다. 어떠한 상황(처리속도의 중요성 or 정확도의 중욧어)에서 무엇을 사용해야할지 모르기에 두 가지 실습을 모두 진행하였다. 두 가지 방식을 사용하면서, one stage, two stage의 속도 및 정확도를 비교하였다.

