
智慧城市街道道路垃圾检测数据集 
---
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f0a2e5acf9804ebaaf51e77de3ed67fc.png)

### 📊 数据集总体统计

| 项目 | 内容 |
|------|------|
| 数据集名称 | 智慧城市街道垃圾检测数据集（Urban Street Litter Detection Dataset） |
| 图像总数 | 3,300 张 |
| 图像分辨率 | 多为 1920×1080 或 1280×720（来自监控摄像头与手机拍摄） |
| 标注格式 | YOLO `.txt` 格式（归一化坐标：`class_id center_x center_y w h`） |
| 配套文件 | 包含 `data.yaml`、训练/验证/测试集划分、完整标签文件 |
| 类别数量 | 28 类常见城市垃圾 |
| 数据质量 | 高精度人工标注，已实测可用于模型训练 |
| 适用模型 | YOLOv5 / YOLOv8 / YOLOv11 等系列目标检测模型 |

---
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/02e8c3a80fdf402a82636fc6311a169a.png)

### 🔢 数据集划分情况

| 数据集类型 | 图像数量 | 占比 | 用途 |
|-----------|----------|------|------|
| 训练集（train） | 2,640 张 | 80% | 模型训练学习特征 |
| 验证集（val）   | 330 张  | 10% | 超参数调优与性能评估 |
| 测试集（test）  | 330 张  | 10% | 最终模型效果测试 |

---
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/85c1e45f7eab472c81c993ed60752e15.png)

### 🗑️ 垃圾类别列表（共 28 类）

| 编号 | 类别英文名 | 中文名称 | 示例 |
|------|------------|----------|------|
| 0 | Plastic_Bottle | 塑料瓶 | 饮料瓶、矿泉水瓶 |
| 1 | Banana_Peel | 香蕉皮 | 果皮类有机垃圾 |
| 2 | Can | 易拉罐 | 铝制饮料罐 |
| 3 | Glass_Bottle | 玻璃瓶 | 啤酒瓶、调料瓶等 |
| 4 | Paper | 废纸 | 包装纸、传单、纸巾（干） |
| 5 | Cigarette_End | 烟头 | 常见街道污染源 |
| 6 | Apple_Core | 苹果核 | 果核类厨余垃圾 |
| 7 | Food_Waste | 食物残渣 | 剩饭、菜叶等 |
| 8 | Takeaway_Box | 外卖盒 | 泡沫或塑料餐盒 |
| 9 | Plastic_Bag | 塑料袋 | 超市购物袋、包装袋 |
| 10 | Wrapper | 包装纸 | 糖果纸、零食包装 |
| 11 | Mask | 口罩 | 一次性医用口罩 |
| 12 | Cardboard | 纸板 | 快递箱、硬纸壳 |
| 13 | Bottle_Cap | 瓶盖 | 塑料或金属瓶盖 |
| 14 | Straw | 吸管 | 塑料/纸质吸管 |
| 15 | Foam_Packaging | 泡沫包装 | 电器内衬、保温箱 |
| 16 | Wet_Tissue | 湿纸巾 | 不可降解清洁用品 |
| 17 | Chewing_Gum | 口香糖 | 地面粘连污渍 |
| 18 | Battery | 电池 | 废旧干电池（有害垃圾） |
| 19 | Syringe | 注射器 | 医疗废弃物（危险品） |
| 20 | Cloth_Rag | 抹布/破布 | 废弃织物 |
| 21 | Toy | 小玩具 | 迷你塑料玩具 |
| 22 | Leaf | 树叶 | 自然掉落物（属园林垃圾） |
| 23 | Stone | 石块 | 小石子、碎砖块 |
| 24 | Branch | 树枝 | 较小断枝 |
| 25 | Dog_Feces | 狗粪 | 宠物排泄物 |
| 26 | Can_Lid | 罐头盖 | 金属罐封口盖 |
| 27 | Broken_Pottery | 破陶瓷 | 碎碗、瓦片等 |

---
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0f951d49136e4b7cabb1c6b6267b867a.png)

### ✅ 配套文件示例：`data.yaml`

```yaml
# data.yaml
train: ./images/train
val: ./images/val
test: ./images/test

nc: 28

names: ['Plastic_Bottle', 'Banana_Peel', 'Can', 'Glass_Bottle', 'Paper',
        'Cigarette_End', 'Apple_Core', 'Food_Waste', 'Takeaway_Box', 'Plastic_Bag',
        'Wrapper', 'Mask', 'Cardboard', 'Bottle_Cap', 'Straw', 'Foam_Packaging',
        'Wet_Tissue', 'Chewing_Gum', 'Battery', 'Syringe', 'Cloth_Rag', 'Toy',
        'Leaf', 'Stone', 'Branch', 'Dog_Feces', 'Can_Lid', 'Broken_Pottery']
```

---

### 💡 应用场景建议
- 智慧城市环卫管理
- 自动清扫机器人导航避障与识别
- 街道环境评分系统
- 公众环保行为监测（AI+监控）
- 垃圾分类AI教育工具

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1e477a9ae1e541d8bb754e3290ea62d3.png)
1
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0d7b89454a094f31b0061072b6b94af9.png)
1
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/3e92416c9b034e658b865c164b4e2433.png)
\*YOLOv11 训练代码（Python 脚本）**，基于 [Ultralytics YOLO](https://github.com/ultralytics/ultralytics) 最新版本编写，支持 `yolov11n/s/m/l/x` \

---

### ✅ `train_yolov11.py` —— 城市街道垃圾检测训练脚本

```python
# train_yolov11.py
from ultralytics import YOLO
import torch
import os
from datetime import datetime

# ========================
# 🛠️ 参数配置区
# ========================
MODEL_NAME = "yolov11s.pt"                # 推荐使用: yolov11n (轻量), yolov11s/m (平衡)
DATA_CONFIG = "data.yaml"                 # 必须与数据集同目录或指定路径
PROJECT_NAME = "runs/litter_detection"    # 项目保存根目录
EXPERIMENT_NAME = f"exp_{datetime.now().strftime('%Y%m%d_%H%M%S')}"  # 自动命名实验
EPOCHS = 150                              # 总训练轮数
BATCH_SIZE = 16                           # 根据 GPU 显存调整：24G 可用 16，16G 建议 8
IMG_SIZE = 640                            # 输入图像尺寸（YOLOv11 支持多尺度）
DEVICE = 0 if torch.cuda.is_available() else 'cpu'  # 使用 GPU 0，如需多卡：[0,1]

# ========================
# 🔍 模型初始化
# ========================
print("🚀 开始训练 城市街道垃圾检测模型...")
print(f"📦 模型: {MODEL_NAME}")
print(f"📊 数据集配置: {DATA_CONFIG}")
print(f"🎯 图像尺寸: {IMG_SIZE}, Batch Size: {BATCH_SIZE}, Epochs: {EPOCHS}")
print(f"📍 设备: {'GPU' if DEVICE != 'cpu' else 'CPU'}")

# 加载预训练模型（自动下载若不存在）
model = YOLO(MODEL_NAME)

# ========================
# ⚙️ 开始训练
# ========================
results = model.train(
    data=DATA_CONFIG,
    epochs=EPOCHS,
    batch=BATCH_SIZE,
    imgsz=IMG_SIZE,
    device=DEVICE,
    project=PROJECT_NAME,
    name=EXPERIMENT_NAME,
    save=True,
    save_period=10,                      # 每10轮保存一次检查点
    exist_ok=False,                      # 防止覆盖已有实验
    
    # 数据增强策略（提升泛化能力）
    hsv_h=0.015,                         # 色调扰动
    hsv_s=0.7,                           # 饱和度变化
    hsv_v=0.4,                           # 明度变化
    degrees=10.0,                        # 随机旋转 ±10°
    translate=0.2,                       # 平移比例
    scale=0.5,                           # 缩放比例
    shear=2.0,                           # 剪切变换
    perspective=0.0001,                  # 透视变换
    flipud=0.0,                          # 上下翻转（不适合倒立垃圾）
    fliplr=0.5,                          # 左右翻转（合理）
    mosaic=1.0,                          # Mosaic 数据增强强度
    mixup=0.1,                           # MixUp 增强
    copy_paste=0.1,                      # Copy-Paste 小目标增强
    
    # 优化器设置
    optimizer='auto',                    # 自动选择 AdamW 或 SGD
    lr0=0.01,                            # 初始学习率
    lrf=0.01,                            # 最终学习率为初始的 1%
    momentum=0.937,
    weight_decay=0.0005,
    
    # 损失函数权重
    box=7.5,
    cls=0.5,
    dfl=1.5,
    
    # 学习率调度
    cos_lr=False,                        # 使用线性衰减（更稳定）
    
    # 提前停止
    patience=30,                         # 30 轮无提升则提前结束
    
    # 其他
    seed=42,                             # 固定随机种子，保证可复现
    workers=4,                           # 数据加载线程数
    close_mosaic=10,                     # 最后10轮关闭 Mosaic，稳定收敛
    val=True,                            # 每轮都验证
    verbose=True
)

print("✅ 训练完成！")
print(f"📈 所有日志与模型保存在: {os.path.join(PROJECT_NAME, EXPERIMENT_NAME)}")
print(f"📁 最佳模型路径: {os.path.join(PROJECT_NAME, EXPERIMENT_NAME)}/weights/best.pt")
print(f"📄 最终模型路径: {os.path.join(PROJECT_NAME, EXPERIMENT_NAME)}/weights/final.pt")
```

---

### 📁 文件结构要求

TX ,确保您的项目目录如下：

```
litter_dataset/
├── images/
│   ├── train/        # 2640 张训练图
│   ├── val/          # 330 张验证图
│   └── test/         # 330 张测试图
├── labels/
│   ├── train/        # 对应 .txt 标注文件
│   ├── val/
│   └── test/
├── data.yaml         # 类别和路径配置
└── train_yolov11.py  # 本训练脚本
```

---

### 🧪 如何运行？

#### 1. 安装依赖（首次）

```bash
pip install ultralytics torch torchvision torchaudio --index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

> 💡 推荐使用清华源加速安装。如需 GPU 支持，请安装 CUDA 版本 PyTorch。

#### 2. 启动训练

```bash
python train_yolov11.py
```

---

### 🔍 推理示例（训练后测试）

```python
from ultralytics import YOLO

# 加载最佳模型
model = YOLO('runs/litter_detection/exp_*/weights/best.pt')

# 进行预测
results = model.predict(
    source='test_images/',      # 图片/视频/文件夹
    conf=0.25,                  # 置信度阈值
    iou=0.45,                   # NMS IOU 阈值
    save=True,                  # 保存带框图像
    project='output',
    name='detection_results'
)
```

---

### 📈 输出内容包括：
- 每轮的 `loss`, `mAP@0.5`, `precision`, `recall`, `F1-score`
- 混淆矩阵（Confusion Matrix）
- PR 曲线、特征图可视化
- 最佳权重 `.pt` 文件

---

仅作参考学习。
