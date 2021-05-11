# SR------flow
cd code
#在imageProcess.py文件中修改地址，改变图像像素大小，使其能被4整除
python imageProcess.py
#在convert_channels文件中修改地址，改为三通道图片
python convert_channels.py
#在imageProvide.py 中修改三次地址以及抽取的比例数，得到train val 以及test 三个图像集
python imageProvide.py
#将图像打包为pklv格式
python prepare_data.py 图像集所在路径
#修改yml文件中的参数
#训练
python train.py -opt ./confs/xxxxx.yml
#损失函数不再明显变化时终止训练，得到一个后缀为pth的模型
