# 🎬 视频脚本生成器 Video Script Generator



[English](#english) | [中文](#chinese)

---

<a name="english"></a>
## 📖 English Documentation

### Project Description

A powerful AI-driven video script generator built with Streamlit and LangChain. This application automatically generates creative video scripts based on user-provided topics, leveraging DeepSeek AI and Wikipedia research to create engaging content.

### Features

- 🤖 **AI-Powered Generation**: Uses DeepSeek AI for intelligent script creation
- 📚 **Wikipedia Integration**: Automatically searches and incorporates relevant information
- ✨ **Customizable Creativity**: Adjust the creativity level from strict to highly creative
- ⏱️ **Duration Control**: Generate scripts for specific video lengths
- 🎯 **Three-Part Structure**: Auto-generates Opening, Middle, and Ending sections
- 🌐 **User-Friendly Interface**: Built with Streamlit for easy interaction

### Tech Stack

- **Frontend**: Streamlit 1.31.1
- **AI Framework**: LangChain 0.1.9
- **LLM Provider**: DeepSeek API
- **Data Source**: Wikipedia API
- **Language**: Python 3.10+

---

## 🚀 Quick Start

### Prerequisites

- Python 3.10 or higher
- pip package manager
- DeepSeek API Key ([Get it here](https://platform.deepseek.com/))

### Installation Steps

#### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd video-script-generator
```

#### 2. Create Virtual Environment (Recommended)
```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# macOS/Linux
python3 -m venv .venv
source .venv/bin/activate
```

#### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

#### 4. Run the Application
```bash
streamlit run main.py
```

#### 5. Access the Application
Open your browser and navigate to:
- **Local**: http://localhost:8501
- **Network**: http://YOUR_IP:8501

---

## 📝 Usage Guide

### Step 1: Enter API Key
- In the sidebar, input your **DeepSeek API Key**
- Click the link to get your API key if you don't have one

### Step 2: Configure Video Parameters
- **Topic**: Enter the subject of your video (e.g., "Artificial Intelligence")
- **Duration**: Set video length in minutes (minimum 0.1)
- **Creativity**: Adjust the slider:
  - `0.0` - More strict and factual
  - `1.0` - More creative and diverse

### Step 3: Generate Script
- Click the **"生成脚本"** (Generate Script) button
- Wait for AI processing (usually 10-30 seconds)

### Step 4: Review Results
The application will generate:
- 🔥 **Attractive Title**
- 📝 **Complete Script** (Opening, Middle, Ending)
- 👀 **Wikipedia Research** (expandable section)

---

## 🛠️ Troubleshooting

### Common Issues

**1. Dependencies Installation Failed**
```bash
# Try upgrading pip first
pip install --upgrade pip
pip install -r requirements.txt
```

**2. Port 8501 Already in Use**
```bash
# Use a different port
streamlit run main.py --server.port 8502
```

**3. API Key Error**
- Verify your DeepSeek API key is valid
- Check if you have sufficient API credits
- Ensure no extra spaces in the API key

**4. Wikipedia Search Timeout**
- Check your internet connection
- Try using a VPN if Wikipedia is blocked in your region

---

## 📦 Project Structure

```
video-script-generator/
│
├── main.py              # Streamlit main application
├── utils.py             # Core script generation logic
├── requirements.txt     # Python dependencies
└── README.md           # This file
```

---

## 🔧 Configuration

### Custom AI Model
Edit `utils.py` to use different models:
```python
model = ChatOpenAI(
    base_url="https://api.deepseek.com/v1",
    api_key=api_key,
    model="deepseek-chat",  # Change to: deepseek-r1
    temperature=creativity
)
```

### Change Wikipedia Language
Edit `utils.py` line 40:
```python
search = WikipediaAPIWrapper(lang="zh")  # Change to: "en" for English
```

---

## 📄 License

This project is open source and available under the MIT License.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

---

<a name="chinese"></a>
## 📖 中文文档

### 项目简介

基于 Streamlit 和 LangChain 构建的 AI 视频脚本生成器。本应用根据用户提供的主题，利用 DeepSeek AI 和维基百科研究自动生成富有创意的视频脚本。

### 功能特点

- 🤖 **AI 智能生成**：使用 DeepSeek AI 进行智能脚本创作
- 📚 **维基百科集成**：自动搜索并整合相关信息
- ✨ **可调节创造力**：从严谨到高度创新的创造力调节
- ⏱️ **时长控制**：为特定视频长度生成脚本
- 🎯 **三段式结构**：自动生成开头、中间和结尾部分
- 🌐 **友好界面**：使用 Streamlit 构建，易于交互

### 技术栈

- **前端**: Streamlit 1.31.1
- **AI 框架**: LangChain 0.1.9
- **LLM 提供商**: DeepSeek API
- **数据来源**: Wikipedia API
- **编程语言**: Python 3.10+

---

## 🚀 快速开始

### 环境要求

- Python 3.10 或更高版本
- pip 包管理器
- DeepSeek API 密钥 ([点击获取](https://platform.deepseek.com/))

### 安装步骤

#### 1. 克隆仓库
```bash
git clone <your-repository-url>
cd video-script-generator
```

#### 2. 创建虚拟环境（推荐）
```bash
# Windows
python -m venv .venv
.venv\Scripts\activate

# macOS/Linux
python3 -m venv .venv
source .venv/bin/activate
```

#### 3. 安装依赖
```bash
pip install -r requirements.txt
```

#### 4. 运行应用
```bash
streamlit run main.py
```

#### 5. 访问应用
在浏览器中打开：
- **本地访问**: http://localhost:8501
- **网络访问**: http://YOUR_IP:8501

---

## 📝 使用指南

### 步骤 1：输入 API 密钥
- 在侧边栏输入您的 **DeepSeek API 密钥**
- 如果没有密钥，点击链接获取

### 步骤 2：配置视频参数
- **主题**：输入视频主题（例如："人工智能"）
- **时长**：设置视频时长（分钟，最小 0.1）
- **创造力**：调节滑块：
  - `0.0` - 更严谨、更真实
  - `1.0` - 更有创意、更多样化

### 步骤 3：生成脚本
- 点击 **"生成脚本"** 按钮
- 等待 AI 处理（通常 10-30 秒）

### 步骤 4：查看结果
应用将生成：
- 🔥 **吸引人的标题**
- 📝 **完整脚本**（开头、中间、结尾）
- 👀 **维基百科搜索结果**（可展开查看）

---

## 🛠️ 故障排除

### 常见问题

**1. 依赖安装失败**
```bash
# 先升级 pip
pip install --upgrade pip
pip install -r requirements.txt
```

**2. 端口 8501 已被占用**
```bash
# 使用其他端口
streamlit run main.py --server.port 8502
```

**3. API 密钥错误**
- 验证 DeepSeek API 密钥是否有效
- 检查 API 额度是否充足
- 确保密钥中没有多余空格

**4. 维基百科搜索超时**
- 检查网络连接
- 如果维基百科被屏蔽，尝试使用 VPN

---

## 📦 项目结构

```
video-script-generator/
│
├── main.py              # Streamlit 主应用
├── utils.py             # 核心脚本生成逻辑
├── requirements.txt     # Python 依赖
└── README.md           # 本文件
```

---

## 🔧 自定义配置

### 更换 AI 模型
编辑 `utils.py` 使用不同模型：
```python
model = ChatOpenAI(
    base_url="https://api.deepseek.com/v1",
    api_key=api_key,
    model="deepseek-chat",  # 可改为: deepseek-r1
    temperature=creativity
)
```

### 更改维基百科语言
编辑 `utils.py` 第 40 行：
```python
search = WikipediaAPIWrapper(lang="zh")  # 改为: "en" 使用英文
```

---

## 📄 开源协议

本项目采用 MIT 开源协议。

---

## 🤝 贡献

欢迎贡献代码、提出问题和功能建议！

---

## 📞 Contact / 联系方式

如有问题或建议，欢迎提交 Issue 或 Pull Request。

---

**Made with ❤️ using Streamlit & DeepSeek AI**
