# 图像去雾项目

## 数据集来源
- [SFSU Synthetic Dataset](https://people.ee.ethz.ch/~csakarid/SFSU_synthetic/)

## 相关论文与代码

### 图像去雾算法
- 论文：何凯明博士基于暗通道先验的单幅图像去雾算法  
  [阅读论文](https://ieeexplore.ieee.org/document/5206515)

- 代码：何凯明博士基于暗通道先验的单幅图像去雾算法  
  [GitHub代码](https://github.com/FengEternity/DehazeFog)

- 图像去雾系统：DehazeNet  
  [GitHub代码](https://github.com/caibolun/DehazeNet)

## 项目架构

```plaintext
dehaze_project/
│
├── data/                   # 数据文件夹
│   ├── raw/                # 原始数据集（有雾图像和无雾图像）
│   ├── preprocessed/       # 预处理后的数据
│   └── augmented/          # 数据增强后的数据（可选）
│
├── models/                 # 存放模型文件
│   ├── dehazenet.py        # 模型定义脚本
│   ├── train.py            # 训练模型脚本
│   └── evaluate.py         # 评估模型脚本
│
├── outputs/                # 输出文件夹
│   ├── logs/               # 训练过程的日志
│   ├── models/             # 存放训练好的模型
│   ├── results/            # 存放去雾结果图像
│   └── checkpoints/        # 存放中间训练检查点
│
├── utils/                  # 辅助函数
│   ├── data_preprocessing.py # 数据预处理相关函数
│   ├── image_utils.py      # 图像处理工具函数（如加载、保存等）
│   └── metrics.py          # 自定义评估指标
│
├── main.py                 # 主入口文件
└── README.md               # 项目说明文件
