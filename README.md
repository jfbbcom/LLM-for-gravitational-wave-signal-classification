这是一个关于大模型首次应用于引力波分类的项目。

# 一、数据说明
真实数据：GW文件夹下，是kaggle网站提供的数据。
模拟数据：events.csv文件为GWOSC网站提供的观测到的引力波的详细数据（https://gwosc.org/eventapi/html/GWTC/）。events_with_duration.csv文件为根据详细数据与模板计算出各个引力波事件的持续时间。真实数据存储于
llamafactory/data/文件夹下。

# 二、训练工具
使用LLAmafactory进行模型的训练。具体的教程可以参考：https://zhuanlan.zhihu.com/p/695287607?utm_source=wechat_session&utm_medium=social&s_r=0
但是对其中的某些文件进行了修改，用于进行准确率的计算、混淆矩阵的绘制（src文件），llamafactory文件中的各个部分与使用过的models可由png显示。

# 三、训练文件
trian.ipynb文件用于清洗、生成数据以及绘制图像等。
llama3_lora_sft.yaml、llama3_merge_config.yaml、llama3_lora_test.yaml，三个文件依次运行，能得到一次模型的训练结果。
last_test_log.py、last_train_log.py为存储运行记录的文件。

