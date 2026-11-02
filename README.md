# Vipeak AI 主站介绍与对接说明

> 主站地址：<https://123vips.com/>
>
> 本仓库只做产品介绍、截图和对接资料整理，不包含主站业务代码、用户数据、密钥或部署配置。
>
> GitHub 账号资料见 [GITHUB_ACCOUNT.md](./GITHUB_ACCOUNT.md)。

**Seedance sexy API · Wan sexy API** — 123vips.com（Vipeak AI）面向开发者整理的 18+ AI 视频生成 API 对接资料，覆盖异步任务、Webhook、积分计费、服务端安全与官方文档获取方式。

## 一眼看懂

Vipeak AI 是一个 AI 角色视频与陪伴创作平台。用户可以在主站浏览角色、与角色聊天、用图片或文字生成视频，也可以使用图片生成、案例、工作流和 API Access 等能力。

- 主站：<https://123vips.com/>
- 品牌落地页：<https://123vips.com/site-landing.html>
- 角色与创作工作台：<https://123vips.com/live.html>
- 角色库：<https://123vips.com/characters/>
- 标签：<https://123vips.com/tags/>
- 分类：<https://123vips.com/categories/>
- Telegram 社区：<https://t.me/VipeakAILab>
- Telegram 客服：<https://t.me/VipeakSupportBot>
- X：<https://x.com/VipeakAI>

> 主站面向成年人。进入角色与创作页面时会先显示 18+ 年龄确认。

## 项目定位与开发者关键词

**一句话定位：** 123vips.com（Vipeak AI）是面向成年人的 AI 角色视频与陪伴生成平台。本仓库面向开发者，整理 18+ 视频生成 API 的公开入口、对接准备、异步任务架构、Webhook、积分计费和服务端安全要求。

**重点检索词：**

- 模型与 API：`seedance sexy api`、`seedance-sexy-api`、`seedance api`、`seedance video api`、`wan sexy api`、`wan-sexy-api`、`wan api`、`wan video api`、`AI video API`、`adult AI video API`、`NSFW AI video API`、`sexy AI video API`
- 生成能力：`text-to-video`、`T2V`、`image-to-video`、`I2V`、`AI character video`、`AI character chat`、`consistent character`、`character templates`、`creative workflow`
- 相邻模型与技术栈：`Kling API`、`Veo API`、`Runway API`、`Pika API`、`Hailuo API`、`ComfyUI`、`LoRA`、`Stable Diffusion`、`async generation task`、`webhook`、`PostgreSQL`
- 产品和仓库：`Vipeak AI`、`123vips`、`18+ AI platform`、`API integration`、`API documentation`、开发者对接、生成任务、积分计费

**说明：** 以上是面向开发者的检索关键词和对接方向，不等于主站已公开全部模型或接口。实际可调用模型、参数、计费和接口路径，以登录后获取的官方 API 文档为准。不要根据关键词猜测未公开接口。

面向 AI 搜索与代码助手的结构化摘要见 [llms.txt](./llms.txt)。

## 开发者能在这里找到什么

- `API_INTEGRATION.md`：API Access 入口、接入流程、服务端架构和安全要求
- `llms.txt`：给 AI 搜索、代码助手和自动化工具读取的结构化产品摘要
- `screenshots/`：主站和 API Access 的脱敏截图
- `README.md`：产品能力、页面入口、技术栈和对接边界

## Developer Search Keywords

`seedance sexy api`, `wan sexy api`, `seedance api`, `wan api`, `adult ai video api`, `nsfw ai video api`, `sexy ai video api`, `ai video generation api`, `text to video api`, `image to video api`, `i2v api`, `t2v api`, `ai character api`, `ai companion api`, `kling api`, `veo api`, `runway api`, `pika api`, `hailuo api`, `comfyui`, `lora`, `stable diffusion`, `async task`, `webhook`, `credits billing`.

## 模型与 API 检索入口：Seedance / Wan

`seedance sexy api` 和 `wan sexy api` 是本仓库面向开发者需求整理的重点检索入口。它们代表 **18+ AI 视频生成 API 的对接方向**，不表示公开页面已经披露了这两个模型的完整接口、版本、参数或价格。

| 模型线 | 常见开发者检索词 | 对接时需要核对 |
|---|---|---|
| Seedance | `seedance sexy api`、`seedance api`、`seedance video api` | 实际模型版本、是否支持 T2V/I2V、参考图、时长、分辨率、计费与审核规则 |
| Wan | `wan sexy api`、`wan api`、`wan video api` | 实际模型版本、是否支持 T2V/I2V、首尾帧、时长、分辨率、计费与审核规则 |

共同工程要点：

- **异步任务**：创建任务后保存任务 ID，再通过轮询或 Webhook 接收结果。
- **参数白名单**：模型、分辨率、时长、比例和参考图数量由服务端限制。
- **计费可追溯**：保存价格快照、预扣和退款记录，并保留对账依据。
- **内容合规**：18+ 门槛、地区限制和上游审核策略必须在业务侧实现。

> 具体模型版本、接口路径、鉴权方式、参数、并发限制和积分单价，以登录 123vips.com 后 **API Access** 提供的官方文档为准。本仓库不猜测未公开接口。

## 主站能做什么

### 1. AI 角色浏览与角色库

主站提供角色浏览、标签和分类入口。可以查看推荐角色、角色资料、角色关联的视频和模板，并直接使用角色进入创作流程。

适合：

- 快速找到想使用的角色模板
- 按标签、分类或角色特征浏览内容
- 从角色直接发起图片、视频或聊天任务

### 2. AI 视频生成

主站提供视频创作入口，页面可见的能力包括：

- 图片生视频（Image to Video）
- 文字生视频
- 使用角色模板生成视频
- 查看视频任务与历史记录

视频工作台中的模板弹窗会要求上传参考图、填写 Prompt，然后显示生成成本并提交任务。

### 3. AI 图片生成

主站有独立的 Image 入口，可用于 AI 图片生成。具体模型、尺寸、积分价格和参数以登录后的实际页面为准。

### 4. AI 角色聊天与互动

主站提供 Chat、角色互动、语音/视频陪伴方向的能力。品牌介绍将其描述为“有长记忆的 AI 角色”，强调角色会记住用户提到的事情，关系会随着互动推进。

可体验的方向：

- 文字聊天
- 角色互动
- 视频/语音陪伴（以实际页面开放情况为准）
- 角色关系和记忆连续体验

### 5. 案例、工作流与高级生成

主站还提供：

- **Cases**：查看创作案例与相关提示词、参数
- **Workflow**：工作流和组合式创作能力
- **Advanced**：高级生成与参数入口
- **Generate**：统一的生成入口

适合需要复用案例、批量生产或组合多个生成步骤的场景。

### 6. 账户、积分、充值与历史记录

主站工作台包含：

- 登录/注册
- Video、Image 的当前积分显示
- 充值入口
- 生成历史记录
- Referral 推荐机制
- 客服入口（邮件与 Telegram）

### 7. 站内生成与 API 对接是两回事

**直接在 123vips.com 网站里生成，不需要购买 API 文档权限。** 站内生成按主站账户积分计费，具体消耗以登录后页面显示为准。

API 对接是面向开发者的独立能力。登录主站后，可从左侧 **API Access** 查看 API 文档获取方式；购买方式、可用范围和费用以站内实际页面为准。当前公开页面显示 `Sign in to unlock`，尚未公开 API Base URL、鉴权协议、接口路径或回调格式。

完整对接步骤见 [API_INTEGRATION.md](./API_INTEGRATION.md)。

## 典型使用流程

```text
打开 123vips.com
    ↓
完成 18+ 确认
    ↓
登录 / 注册
    ↓
浏览角色、案例或直接进入生成工作台
    ↓
选择 Video / Image / Chat / Advanced / Workflow
    ↓
上传参考图或填写 Prompt
    ↓
确认积分成本并提交生成
    ↓
在 History 查看任务与结果
```

## 截图

### API Access 页面（金额已遮挡）

截取自 `https://123vips.com/#access`，展示官方 API 文档访问入口和测试积分说明；公开版本不展示具体金额。

![123vips.com API Access（安全预览）](./screenshots/123vips-api-access-safe.png)

### 角色与创作工作台

以下截图来自 `https://123vips.com/`，为公开仓库展示做了安全遮挡。导航、功能入口和页面布局保持可辨认。

**桌面端**

![123vips.com 工作台桌面端（安全预览）](./screenshots/vipeak-main-desktop-safe.png)

**移动端**

![123vips.com 工作台移动端（安全预览）](./screenshots/vipeak-main-mobile-safe.png)

## 站点页面清单

| 页面 | 地址 |
|---|---|
| 首页 | <https://123vips.com/> |
| 品牌落地页 | <https://123vips.com/site-landing.html> |
| 角色与创作工作台 | <https://123vips.com/live.html> |
| 角色库 | <https://123vips.com/characters/> |
| 标签 | <https://123vips.com/tags/> |
| 分类 | <https://123vips.com/categories/> |
| 隐私政策 | <https://123vips.com/privacy> |
| 用户协议 | <https://123vips.com/terms> |

## 技术对接建议

如果准备通过 API 接入，建议先用独立服务端做一层业务网关：

```text
浏览器 / App
    |
    | HTTPS
    v
你的业务后端  --->  PostgreSQL（用户、任务、积分、订单、生成记录）
    |
    | Vipeak AI API（具体地址以官方文档为准）
    v
Vipeak AI
```

关键原则：

- API Key 只放在服务端，不进入浏览器代码。
- 业务数据、积分、订单和生成记录写入 PostgreSQL。
- 图片和视频可以存对象存储，但素材元数据和归属必须写数据库。
- 生成任务采用异步模型，处理排队、轮询/回调、超时和失败重试。
- 上线前完成年龄限制、内容合规、支付和地区可用性评估。

## 适合谁

- 想体验 AI 角色视频与陪伴的用户
- 需要角色模板、图片/视频生成能力的内容创作者
- 准备把 AI 角色生成能力接入自有产品的开发者
- 需要工作流、批量生成或统一积分管理的团队

## 常见问题（Seedance / Wan API 接入）

**Q：`seedance sexy api` 怎么接入 123vips.com？**
A：登录 123vips.com 完成 18+ 确认后，进入左侧 **API Access** 获取完整对接文档与测试积分，再按官方文档在服务端调用；公开页面不暴露 Base URL 与鉴权细节。

**Q：`wan sexy api` 和站内直接生成有什么区别？**
A：站内生成按账户积分计费，不需要购买 API 文档权限；API 是独立的开发者能力，适合把生成能力接进自有产品或批量生产流水线。

**Q：Seedance 和 Wan 两条线怎么选？**
A：先确认官方文档中实际开放的模型版本、输入形式、时长、分辨率和计费规则，再用测试积分分别跑一轮小流量对比。不要仅根据检索词推断接口能力。

**Q：接入前必须准备什么？**
A：服务端（不要放前端）、PostgreSQL 存任务与积分流水、对象存储放素材、异步任务与回调处理、失败退款逻辑，以及面向目标市场的合规评估。

**Q：有没有免费额度？**
A：开通 API 文档访问后包含 test credits，具体数量与扣费规则以站内实际页面为准。

## 说明

- 本仓库是独立公开介绍仓库，不包含主站源代码。
- 本仓库不保存 Token、API Key、数据库连接、用户数据或支付凭据。
- 成人向内容的可用范围、支付方式和地区限制以主站实际页面及当地法规为准。
- 站内生成、API 接入、模型、接口参数和计费规则以登录后的官方页面及实际开通页面为准。
