# RSTnet：实时语音-文本基础模型工具包（持续更新中）

构建能够理解和生成语音的实时语音-文本基础模型已引起广泛关注，ChatGPT-4o和Moshi等典型范例已展现出其潜力。然而，这类模型的训练仍面临诸多挑战。为此，我们推出RSTnet——一个专为开发实时语音-文本基础模型设计的开源平台。该工具包提供从数据处理、预训练到微调的完整框架，基于实时语音对话模型（Moshi）和通用音频生成模型（UniAudio）等前沿研究构建，主要包含四大核心模块：
(1) 数据准备    
(2) 流式音频编解码模型    
(3) 语音-文本基础模型   
(4) 基准测试与评估。   

## 最新动态
• [x] 2025.3.4 发布RSTnet第二版，支持语音-文本基础模型预训练，详见MLLM_v2模块   
• [x] 2024.10.7 发布RSTnet初始版本   

## 参与贡献
本项目持续开发中，欢迎通过以下方式参与：
• [1] 提交issue或PR修复问题   
• [2] 提供数据收集、流式编解码或语音-文本模型的新思路   
• [3] 申请成为项目作者（联系邮箱：dcyang@se.cuhk.edu.hk）   

## 安装指南
```bash
conda create -n RSTnet python=3.12   
conda activate RSTnet   
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121   
pip install tqdm librosa==0.9.1 matplotlib omegaconf einops   
pip install vector_quantize_pytorch tensorboard deepspeed peft   
```

## 技术报告
完整技术文档详见：https://github.com/yangdongchao/RSTnet/blob/main/RSTnet.pdf   

## 数据处理管道
详细说明即将更新，请关注DataPipeline模块

## 音频编解码器
当前已复现MimiCodec，未来将集成更多先进流式音频编解码方案

## 多模态大模型
已发布功能包括：
1. Moshi模型微调代码
2. 语音-文本基础模型预训练方案
核心优势：   
• 兼容LLAMA/Gemma/Mistral/Phi/StableLM/Qwen等主流大模型架构   
• 支持LoRA微调技术降低GPU资源消耗   
• 提供完整模型训练方案（需充足GPU资源）   

## 参考文献
本项目的流式音频编解码与语音-文本模型实现基于以下代码库：   
https://github.com/kyutai-labs/moshi   
https://github.com/yangdongchao/UniAudio   

## 引用格式
```bibtex
@techreport{RSTnet,
  title={RSTnet: Real-time Speech-Text Foundation Model Toolkit},
  author={RSTnet team},
  journal={Technical report},
  year={2024}
}
```
```bibtex
@techreport{kyutai2024moshi,
    author = {Alexandre D\'efossez and Laurent Mazar\'e and Manu Orsini and Am\'elie Royer and
              Patrick P\'erez and Herv\'e J\'egou and Edouard Grave and Neil Zeghidour},
    title = {Moshi: a speech-text foundation model for real-time dialogue},
    institution = {Kyutai},
    year={2024},
    month={September},
    url={http://kyutai.org/Moshi.pdf},
}
```
```bibtex
@article{yang2023uniaudio,
  title={UniAudio: An Audio Foundation Model Toward Universal Audio Generation},
  author={Dongchao Yang, Jinchuan Tian, Xu Tan, Rongjie Huang, Songxiang Liu, Xuankai Chang, Jiatong Shi, Sheng Zhao, Jiang Bian, Xixin Wu, Zhou Zhao, Helen Meng},
  journal={arXiv preprint arXiv:2310.00704},
  year={2023}
}
```
