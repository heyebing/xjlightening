<div align="center">
  <h1>📘 西交闪学 · XJTU FlashLearn</h1>
  <p><em>智能课堂记录 · AI随堂出题 · 学习资源传承</em></p>
  <p>
    <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android"/>
    <img src="https://img.shields.io/badge/Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin"/>
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
    <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask"/>
    <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"/>
    <img src="https://img.shields.io/badge/LLM-API-8A2BE2?style=for-the-badge" alt="LLM API"/>
  </p>
  <p>
    <a href="#-功能亮点">功能亮点</a> •
    <a href="#-技术栈">技术栈</a> •
    <a href="#-快速开始">快速开始</a> •
    <a href="#-项目结构">项目结构</a> •
    <a href="#-致谢">致谢</a>
  </p>
</div>

---

## 📖 项目简介

**西交闪学 (XJTU FlashLearn)** 是一款专为高校课堂设计的 Android 辅助学习应用。它帮助学生高效完成课堂笔记（文字/录音/拍照）、接收课件与作业通知、扫码签到，并通过 **大模型 AI** 根据老师讲解内容自动生成自测试题。同时独创 **“学长学姐圣遗物”** 资源共享审核机制，让往届作业、笔记得以传承。

> 本仓库包含 Android 客户端源码、服务端 API 及数据库脚本，项目完全开源。

---

## ✨ 功能亮点

| 模块 | 核心能力 |
|:---|:---|
| 📝 **课堂笔记** | 文字+录音同步+拍照矫正；按课程分类/标签/全文搜索；导出 PDF/TXT |
| ✅ **课堂考勤** | 动态二维码 + 地理位置双重校验；自动统计出勤率，导出名单 |
| 📚 **课件与资料** | 教师上传 PPT/PDF/图片；学生离线缓存、收藏 |
| ⏰ **作业与通知** | 作业发布/截止提醒；重要调课/考试推送 |
| 🗓️ **课程表管理** | 手动导入/编辑课表；上课前自动提醒；与笔记/考勤/课件一键跳转 |
| 🤖 **AI 随堂出题** | 基于大模型分析授课内容（语音转文字/课件文本），自动生成选择题/填空题/简答题并提供解析 |
| 🧑‍🎓 **学习资源共享（圣遗物）** | 学生上传往年作业/答案/笔记，经教师/助教审核后公开，形成代际传承库 |

---

## 🛠️ 技术栈

### 客户端
- **语言**: Kotlin / Java  
- **IDE**: Android Studio  
- **关键库**: CameraX, MediaRecorder, ZXing (二维码), Retrofit (网络), Room (本地存储)

### 服务端
- **语言**: Python 3  
- **框架**: Flask  
- **数据库**: MySQL (开发可用 SQLite)  
- **部署**: CentOS 7 / 阿里云 ECS

### AI 集成
- 调用大模型 API（讯飞星火 / 百度文心 / DeepSeek）生成试题

---

## 🚀 快速开始

### 前置条件
- Android Studio Arctic Fox 或更高版本
- JDK 11
- Python 3.8+ (如需运行本地服务端)
- MySQL 5.7+ (可选)

### 克隆仓库
```bash
git clone https://github.com/your-username/xjtu-flashlearn.git
cd xjtu-flashlearn
运行 Android 客户端
用 Android Studio 打开 client/ 目录

同步 Gradle 并连接 Android 设备/模拟器

点击运行 ▶️

启动本地服务端（可选）
bash
cd server
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py
默认服务端地址 http://localhost:5000，请在客户端 config.gradle 中修改 BASE_URL。
```

## 📁 项目结构
text
xjtu-flashlearn/  

├── client/  # Android 客户端源码  
│   ├── app/                 # 主模块 (笔记/考勤/课件/课表/AI出题)  
│   └── README.md  
├── server/                   # Flask 服务端  
│   ├── app.py  
│   ├── models.py  
│   ├── requirements.txt  
│   └── uploads/              # 课件与共享资源存储
├── docs/                     # 设计文档、用户手册
├── database/                 # SQL 建表脚本
└── README.md  

## 大模型 API 由 讯飞星火 / DeepSeek 提供

## 图标资源来自 Material Icons
## 🙏 致谢
### 感谢西安交通大学软件工程课程组的朝乾夕惕，也感谢各位小组成员的支持。
