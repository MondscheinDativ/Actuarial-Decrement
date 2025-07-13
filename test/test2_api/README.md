# 保险精算API测试套件

完整的API测试解决方案，包含测试脚本和模拟服务，用于验证保险精算系统的核心功能。

## 测试范围

1. **数据管道功能**
   - 自定义数据上传
   - 数据清洗处理
   - 数据质量报告生成

2. **分析功能**
   - 获取可用模型列表
   - 获取模型详细信息
   - 运行死亡率预测分析

3. **结果对比功能**
   - 获取可对比项目
   - 运行模型对比分析

## 文件结构

```
actuarial-api-tests/
├── test_api.py         # 主测试脚本
├── mock_server.py      # API模拟服务
├── requirements.txt    # Python依赖
└── README.md           # 使用说明
```

## 快速开始

### 1. 安装依赖
```bash
pip install -r requirements.txt
```

### 2. 启动模拟服务
```bash
python mock_server.py
```

### 3. 运行测试
```bash
python test_api.py
```

### 4. 查看结果
测试结果将直接在终端输出：
```
🚀 开始运行API测试套件
📡 基础URL: http://localhost:5000
📊 测试数据集: [{"age": 30, "year": 2020, "mortality": 0.001}, ...

test_api.py::TestDataPipeline::test_upload_custom_data 
--------------------------------------------------------
测试自定义数据上传...
...
✅ 测试完成! 退出代码: 0
```

## 生成HTML报告
```bash
pytest test_api.py --html=test_report.html
```

## 测试结果示例
- 阿里云服务器安全组限制外部计算机访问，无法获取html测试结果，但终端返回结果显示测试全部通过

## 技术栈
- Python 3.6+
- pytest 测试框架
- Flask 模拟服务
- Requests HTTP客户端

## 贡献指南
欢迎提交Issue和Pull Request：
1. Fork 项目仓库
2. 创建特性分支 (`git checkout -b feature/new-tests`)
3. 提交更改 (`git commit -am 'Add new test cases'`)
4. 推送分支 (`git push origin feature/new-tests`)
5. 创建Pull Request
