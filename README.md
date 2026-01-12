# Algorithm-integration
算法开发集成项目

代码框架预分配：（随时更新）
algorithm-project/                 # 单仓库，多模块
├── build/                         # 构建脚本 & Dockerfile
│   ├── build.sh                   # 一键编译、测试、打包
│   ├── Dockerfile                 # 推理/训练镜像
│   └── docker-compose.yml         # 本地联调
├── framework/                     # 通用算法框架（可独立 git submodule）
│   ├── core/                      # 算法基类、公共算子
│   ├── utils/                     # 日志、配置、可视化
│   └── third_party/               # 重新编译的 OpenCV、TensorRT 等
├── algorithms/                    # 各算法子模块
│   ├── det_yolov8/                # 检测算法示例
│   │   ├── cfg/                   # 超参、yaml
│   │   ├── data/                  # 少量样例数据（<50 M）
│   │   ├── weights/               # 预训练权重（占位，真实权重放对象存储）
│   │   ├── export.py              # 转 ONNX / TensorRT
│   │   └── infer.py               # 推理入口
│   └── cls_efficientnet/
├── data/                          # 大数据用 Git-LFS 或对象存储
│   ├── README.md                  # 数据说明 + 下载脚本
│   └── lfs/.gitattribute          # *.zip filter=lfs
├── models/                        # 版本化模型（只保留 metadata）
│   ├── det_yolov8_v1.0.onnx       # 软链或占位
│   └── registry.json              # 模型名、版本、md5、下载地址
├── tests/                         # pytest / unittest
├── deploy/                        # 部署模板
│   ├── k8s/                       # yaml 模板
│   └── helm/                      # Helm Chart
├── docs/                          # 技术方案、接口文档
└── .gitlab-ci.yml / .github/workflows/
