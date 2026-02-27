# 🚀 OpenClaw AI助手完整框架

> **一键部署完整的AI助手系统**
>
> 包含7步深度使用法、4层模型池、3层记忆体系、11个定时任务

---

## ✨ 特性

- ✅ **7步深度使用法** - 智能备份、模型池、会话识别、压缩、铁律、学习、进化
- ✅ **4层模型池** - 高速/智能/文本/视觉，自动切换
- ✅ **3层记忆体系** - 工作/短期/长期，持续进化
- ✅ **11个定时任务** - 自动化运行，无需人工干预
- ✅ **Heartbeat机制** - 让记忆"活"起来
- ✅ **一键安装** - 3分钟完成部署

---

## 📦 快速开始

### 方法1：自动安装（推荐）

```bash
# 下载并运行安装脚本
cd ~/.openclaw/workspace
git clone [仓库地址] .
chmod +x install.sh
./install.sh
```

### 方法2：手动安装

```bash
# 1. 创建目录
mkdir -p ~/.openclaw/workspace/{config,scripts,data,memory,skills,logs}

# 2. 复制文件
# 将 config/ 和 scripts/ 目录复制到 ~/.openclaw/workspace/

# 3. 安装ClawHub
npm install -g clawhub

# 4. 配置定时任务
openclaw cron add --name "heartbeat-check" --cron "*/30 * * * *" --system-event "heartbeat_check"
```

---

## 📚 核心功能

### 1️⃣ 智能备份机制

**触发条件**: 24小时 或 10K文件变化
**备份策略**: 7天轮换（周一~周日）

```bash
# 手动备份
bash ~/.openclaw/workspace/scripts/smart-backup.sh

# 手动恢复
bash ~/.openclaw/workspace/scripts/auto-restore.sh
```

---

### 2️⃣ 四层模型池

| 模型池 | 主模型 | 用途 |
|:---|:---|:---|
| 高速池 | glm-4.7 | 快速响应 |
| 智能池 | glm-5 | 复杂推理 |
| 文本池 | kimi-k2.5 | 长文本 |
| 视觉池 | glm-4.6v | 图片/视频 |

**自动切换**: 根据任务类型自动选择合适的模型池

---

### 3️⃣ Heartbeat记忆维护

**每30分钟自动执行**:
- 检查紧急事项
- 整理记忆
- 清理日志
- 检查提醒

**每日维护**:
- 提取重要决策
- 更新长期记忆

**每周维护**:
- 回顾记忆
- 清理旧文件

---

### 4️⃣ 每日进化报告

**每天22:00自动生成**:
- 今日学习统计
- 错误总结
- 固化技能建议
- 明日改进计划

---

## 🎯 使用示例

### 示例1：自动任务识别

```
用户: 帮我分析一下数据

AI: [自动识别] 任务属于复杂推理
    [自动切换] 使用智能池
    [执行] 分析完成
```

### 示例2：陌生任务处理

```
用户: 帮我处理PDF

AI: [识别] 陌生任务
    [学习] 搜索ClawHub
    [安装] pdf-skill
    [执行] 处理完成
```

---

## 📊 定时任务列表

| 任务 | 频率 | 说明 |
|:---|:---|:---|
| heartbeat-check | 每30分钟 | 记忆维护 |
| daily-evolution | 22:00 | 每日进化报告 |
| model-health-check | 每6小时 | 模型池健康检查 |
| smart-backup | 每小时 | 智能备份 |

---

## 🔧 自定义配置

### 修改身份信息

编辑 `~/.openclaw/workspace/IDENTITY.md`:

```markdown
- **Name:** 你的AI助手名称
- **Role:** 助手角色定位
```

### 修改用户信息

编辑 `~/.openclaw/workspace/USER.md`:

```markdown
- **Name:** 用户名称
- **Timezone:** 时区
```

### 修改模型池

编辑 `~/.openclaw/workspace/config/model-pools.json`:

```json
{
  "pools": {
    "fast": {
      "primary": "你的模型",
      "fallback": "备用模型"
    }
  }
}
```

---

## 📖 完整文档

查看完整框架文档：
```bash
cat ~/.openclaw/workspace/docs/openclaw-ai-assistant-framework.md
```

---

## 🆘 常见问题

### Q: 定时任务没有运行？

```bash
# 检查定时任务状态
openclaw cron list

# 手动触发测试
python3 ~/.openclaw/workspace/scripts/heartbeat-check.py
```

### Q: 技能安装失败？

```bash
# 检查ClawHub CLI
clawhub --version

# 重新安装
npm install -g clawhub --force
```

### Q: 模型池不健康？

```bash
# 运行健康检查
python3 ~/.openclaw/workspace/scripts/model-health-check.py

# 查看状态
cat ~/.openclaw/workspace/data/model-health-status.json
```

---

## 📝 更新日志

### v2.0 (2026-02-27)
- ✅ 完成7步深度使用法
- ✅ 添加Heartbeat机制
- ✅ 优化模型池配置
- ✅ 增强记忆维护

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

---

## 📄 许可证

MIT License

---

_框架版本: v2.0_
_创建时间: 2026-02-27_
