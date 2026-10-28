# campus-vibe-169 · 大学生学习科学版 Vibe 科普短视频技能（16:9 横版）

> 基于 **dy-hashiqi/VibeDS-skill**（`hyperframes-vibe-169`，作者：哈士奇）改造的垂直扩展版本，已获原作者授权发布。上游框架 **HyperFrames** 由 **HeyGen** 开源（Apache-2.0，仓库：https://github.com/heygen-com/hyperframes）。

为**豆包工作「本地电脑」模式**设计的第三方技能：一句分镜脚本 → 自动生成面向大学生群体的 16:9 横版「Vibe 知识科普」短视频工程（HTML + GSAP 时间线）→ 写入本地 `index.html` → `lint` 校验 → `preview` 预览 → `render` 导出 MP4。

## 与原版（hyperframes-vibe-169）的区别

| 新增内容 | 说明 |
|---|---|
| **大学生赛道垂直知识库** | `references/campus-science-kp.md`：17 个选题（学习效率/考试考证/校园生活/认知心理）+ 三段式文案模板 + 三级变现路径 + 资料包体系 |
| **大学生专属示例工程** | `examples/college-memory-16-9/`：40 秒《为什么背了就忘》完整示例（5 镜，含引流钩子设计），0 error 0 warning |
| **垂直模式接入** | SKILL.md 新增「大学生赛道垂直模式」：收到大学生主题任务时自动调用知识库流程 |
| **变现闭环设计** | 每条视频内置引流钩子（评论区扣字领资料），配合三级变现路径（流量分成 → 私域资料包 → 课程产品） |

## 目录结构

```
campus-vibe-169/
├── SKILL.md                        # 技能主体（含大学生赛道垂直模式）
├── references/
│   ├── campus-science-kp.md        # ★ 大学生赛道知识库（垂直资产）
│   ├── hyperframes-contract.md     # HyperFrames 组合契约精编
│   └── documentary-director.md     # 纪录片导演规范
├── examples/
│   ├── college-memory-16-9/        # ★ 大学生记忆科学示例（本版新增）
│   ├── entropy-16-9/               # 熵增科普示例
│   └── sleep-tired-16-9/           # 越睡越累示例
├── assets/                         # gsap.min.js 等本地资源
├── LICENSE.md                      # 原技能包授权协议（v1.0）
└── README.md
```

## 安装（豆包工作｜本地电脑模式）

### 1. 本机环境（一次性装好）
- Node.js ≥ 22（`winget install OpenJS.NodeJS.LTS` 或 nodejs.org 下载 LTS）
- FFmpeg（`winget install Gyan.FFmpeg`）
- 验证：`node -v && ffmpeg -version | head -1 && npx -y hyperframes@latest doctor`
- 每个项目执行一次：`npx hyperframes init <项目名>`

### 2. 导入技能（二选一）
- **方式 A（上传 zip）**：豆包 PC 客户端 →「插件·技能·伙伴」→「技能」→「+ 添加」→「上传技能」→ 选择 `豆包技能包-campus-vibe-169.zip`
- **方式 B（对话新建）**：「与豆包对话新建技能」，粘贴 `SKILL.md` 全文，保存

### 3. 新建工作任务
「新工作任务」→ 工作设备选**本地电脑** → 授权 HyperFrames 项目文件夹 → 启用技能 `campus-vibe-169`

## 使用示例

```
使用 campus-vibe-169 技能（大学生赛道模式），制作 40 秒 16:9 Vibe 视频，主题：为什么背了就忘？面向大学生群体，结尾带引流钩子。
```

豆包会自动：读知识库选题 → 生成分镜脚本给你确认 → 生成 `index.html` → `lint` 校验 → `preview` 预览；确认后 `render` 导出 MP4。

## 授权与版权

- 本技能包基于 **VibeDS-skill**（© 2026 哈士奇，vibeds_hashiqi@163.com）改造，**已获原作者授权发布**，保留原 `LICENSE.md` 全部条款与署名；
- 内含 **GSAP 3.x**（GreenSock 出品），另行单独使用请遵守 greensock.com 标准许可；
- 上游 **HyperFrames** 为 Apache-2.0 开源（HeyGen），本技能与其无隶属关系；
- 使用本技能制作并发布的视频归制作者所有，建议标注「基于 VibeDS-skill 技能包制作」。
