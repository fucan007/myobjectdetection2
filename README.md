# myobjectdetection2
本次作业主要历程如下
一，根据quiz-w8-data做成TFrecord
1)安装ubuntu系统搭建Ubuntu环境。Ubuntu自带Python2.7和Python 3.5，
2)根据https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/installation.md
的内容安装object_detection模块。(其中根据报错内容和百度查询完成相关Python库的安装，如Python-tk,numpy等)
3)修改create_pet_tf_record.py:
删除代码中所有关于faces_only和mask的代码，设定复合自己电脑环境的路径。
由于给的数据集没有trainval.txt，所以采用os.listdir(image_dir) 作为 examples_list
原代码中main函数每100次才输出一次log，由于数据集较小，改为每次都输出log
(代码参考https://github.com/mengnimei/myobjectdetection2/blob/master/research/object_detection/dataset_tools/create_pet_tf_record.py)
4)运行命令行:
    python3 object_detection/dataset_tools/create_pet_tf_record.py \
        --label_map_path=/home/mengxi/Documents/quiz-w8-data/labels_items.txt \     
        --data_dir=/home/mengxi/Documents/quiz-w8-data \
        --output_dir=/home/mengxi/Documents/quiz-w8-data
   然后生成pet_train.record和pet_val.record数据wenli
