# Algorithm-integration
算法开发集成项目

代码框架预分配：（随时更新）
algorithm-project/
├── build/
│   ├── build.sh
│   ├── Dockerfile
│   └── docker-compose.yml
├── framework/
│   ├── core/
│   ├── utils/
│   └── third_party/
├── algorithms/
│   ├── det_yolov8/
│   │   ├── cfg/
│   │   ├── data/
│   │   ├── weights/
│   │   ├── export.py
│   │   └── infer.py
│   └── cls_efficientnet/
├── data/
│   ├── README.md
│   └── lfs/.gitattributes
├── models/
│   ├── det_yolov8_v1.0.onnx
│   └── registry.json
├── tests/
├── deploy/
│   ├── k8s/
│   └── helm/
├── docs/
└── .gitlab-ci.yml
