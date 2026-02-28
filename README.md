# OpenClaw AI Assistant Framework

一个专业、高效、自主成长的AI助手框架，专为AI自媒体博主设计。

## ✨ 特性

### 🚀 核心能力
- **7步深度使用法**：智能备份、模型池、会话识别、上下文压缩、任务铁律、陌生任务处理、自我进化
- **24小时定向学习**：根据时段自动学习相关技能（视觉创作 + 自媒体运营）
- **AI自我成长**：Skill深度学习、经验总结、知识整合、创造新能力
- **3层记忆体系**：工作记忆、短期记忆、长期记忆
- **10个定时任务**：自动维护、学习、进化、报告

### 📊 模型池体系
- 高速池：zai/glm-4.7（快速响应）
- 智能池：zai/glm-5（复杂推理）
- 文本池：zai/glm-5（长文本）
- 视觉池：zai/glm-4.6v（图片/视频）

### 🎯 24小时学习规则
- 前12小时（00:00-12:00）：视觉创作时段
  - 图像生成、提示词工程
  - 视频制作、剪辑工具
  - 视觉优化、设计工具
- 后12小时（12:00-24:00）：自媒体运营时段
  - 内容创作、文案写作
  - 社交媒体、互动运营
  - 数据分析、自动化营销

## 🚀 快速开始

### 1. 安装

```bash
git clone https://github.com/Work-Fisher/openclaw-ai-assistant-framework.git
cd openclaw-ai-assistant-framework
chmod +x install.sh
./install.sh
```

### 2. 配置

编辑 `config/model-pools.json` 配置模型池：
```json
{
  "pools": {
    "fast": {"primary": "zai/glm-4.7", "fallback": "zai/glm-4.7"},
    "smart": {"primary": "zai/glm-5", "fallback": "zai/glm-5"},
    "text": {"primary": "zai/glm-5", "fallback": "zai/glm-4.7"},
    "vision": {"primary": "zai/glm-4.6v", "fallback": "zai/glm-4.6v"}
  }
}
```

### 3. 启动定时任务

```bash
# 添加定时任务
openclaw cron add --name "install-skills-infinite" --cron "0 * * * *" ...
openclaw cron add --name "heartbeat-notify" --cron "*/30 * * * *" ...
openclaw cron add --name "daily-evolution" --cron "0 22 * * *" ...
openclaw cron add --name "daily-growth-report" --cron "0 9 * * *" ...
```

## 📚 文档

- [完整框架文档](docs/openclaw-ai-assistant-framework.md)
- [AI自我成长计划](docs/ai-self-evolution-plan.md)
- [Skill深度学习机制](docs/skill-deep-learning.md)
- [上下文压缩机制](docs/context-compression-mechanism.md)
- [每日成长报告机制](docs/daily-growth-report-mechanism.md)

## 🔧 核心脚本

- `learn-skill-cli.js` - 技能学习脚本（24小时定向学习）
- `scripts/extract-skill-knowledge.py` - Skill知识提取脚本
- `scripts/heartbeat-check.py` - Heartbeat检查脚本
- `scripts/daily-evolution.py` - 每日进化报告脚本
- `scripts/model-health-check.py` - 模型健康检查脚本

## 📊 定时任务（10个）

### 维护类
1. heartbeat-notify - 每30分钟
2. model-health-check - 每6小时

### 学习类
3. install-skills-infinite - 每小时（24小时定向学习）

### 进化类
4. daily-evolution - 每天22:00
5. daily-growth-report - 每天09:00

## 🎯 版本历史

### v3.0（2026-02-28）
- ✅ 24小时定向学习系统
- ✅ AI自我成长机制
- ✅ Skill深度学习机制
- ✅ 经验总结机制
- ✅ 知识整合机制
- ✅ 完整框架固化

### v2.0（2026-02-27）
- ✅ 7步深度使用框架
- ✅ 4层模型池体系
- ✅ 3层记忆体系
- ✅ 11个定时任务

## 🤝 贡献

欢迎贡献！请查看 [贡献指南](CONTRIBUTING.md)

## 📄 许可证

MIT License

## 🙏 致谢

感谢 OpenClaw 提供的强大框架支持。

---

**当前版本**：v3.0（自我成长版）
**最后更新**：2026-02-28

🚀 持续进化中...
