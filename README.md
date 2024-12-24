# 视频去字幕工具

## 项目结构说明

```
shipingquzimu/
├── src/            # 源代码目录
│   ├── downloader/     # 视频下载模块
│   ├── processor/     # 视频处理模块
│   └── remover/       # 字幕移除模块
├── config/        # 配置文件目录
├── utils/         # 工具函数目录
├── tests/         # 测试文件目录
├── temp/          # 临时文件目录
└── output/        # 输出文件目录
```

## 目录用途说明

- src/: 主要源代码目录
  - downloader/: 负责从各平台下载视频
  - processor/: 视频处理相关代码
  - remover/: 字幕识别和移除相关代码
- config/: 存放配置文件
- utils/: 通用工具函数
- tests/: 单元测试和集成测试
- temp/: 存放处理过程中的临时文件
- output/: 存放处理完成的视频文件
