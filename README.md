# Skill 2.0：模块化 Skill 中间件

> **Skill 不必全局可用——清晰拆成一个部分，就能为我们所用。**
> 从 Skill 1.0（整体封装）到 Skill 2.0（模块化中间件），把研究能力拆成
> SKILL.md / knowledge / templates / data_contract / scripts / config 六类独立模块，
> 每类模块具备 IN/OUT/DEP 接口契约，可被单独调用、单独测试、单独版本化。

## 📖 在线演示

- **技术架构手册（在线阅读）**：`https://github.com/timyefi/skill20-arch` → `/architecture.html`（或站内部署地址）
- **工作论文 CN**：[Skill2_0_模块化中间件_工作论文_CN.pdf](paper/Skill2_0_模块化中间件_工作论文_CN.pdf)
- **Working Paper EN**：[Skill2_0_Modular_Middleware_WorkingPaper_EN.pdf](paper/Skill2_0_Modular_Middleware_WorkingPaper_EN.pdf)

## 架构概览

```
六类独立模块（每个模块有独立 IN/OUT/DEP 契约，可单取）
skill-XXX/
├── SKILL.md          ← 激活与路由（触发条件 + 视角清单 + 模块索引）
├── knowledge/        ← 知识模块（公式 + 阈值 + 案例 + 回验基线）
├── templates/        ← 输出模板模块（表 / 图 / 文字形态）
├── data_contract/    ← 数据契约模块（字段定义，与数据源解耦）
├── scripts/          ← 可执行脚本模块（取数引擎 / 计算引擎，自包含）
└── config/           ← 配置模块（参数 / 路由 / 版本）

五层中间件（每层独立可替换）
输出层（Output）       Word │ 看板（fioutput Navy）│ 微信 │ PPT
计算层（Compute）       公式引擎 │ 指标计算 │ 视角判定
知识层（Knowledge）     knowledge/（公式 + 阈值 + 案例 + 回验基线）
取数层（Data Access）   data_contract 映射 │ 取数引擎（自包含）
数据源层（Source）      iFinD │ Wind │ AKShare │ 本地历史库 │ 自建模型
```

## 为什么模块化：三个论据

| 论据 | 说明 |
|------|------|
| 激活成本 | Skill 1.0 全局可用 → 全量注入上下文；Skill 2.0 默认不激活，按路径指名加载，把全量注入降为按需注入 |
| 契约独立 | 一个模块有自己的 IN/OUT/DEP 契约，调用方只要满足输入声明即可运行，不必理解 Skill 其余部分 |
| 跨库组合 | 复用单位从 Skill 降到模块后，判断逻辑可被多张数据库引用，无需复制整套数据库 |

## 文档清单

| 文件 | 说明 |
|------|------|
| `architecture.html` | 技术架构手册（自包含 HTML，fioutput Navy 设计体系） |
| `paper/Skill2_0_模块化中间件_工作论文_CN.pdf` | 中文工作论文 |
| `paper/Skill2_0_Modular_Middleware_WorkingPaper_EN.pdf` | English working paper |
| `docs/skill-matrix.md` | 已发布手册矩阵（佐证模块粒度的生产运行） |

## 集成模式

1. **全流程使用**：加载整套 Skill，用于端到端研究管线；
2. **只取一个模块**：按路径指名加载所需模块（如只取取数引擎），其余不加载；
3. **数据源替换**：切换数据商只改取数层，上层零感知；
4. **输出形态切换**：同一份计算，换输出模板即可出 Word/看板/微信/PPT。

## 引用

```
Ye Qing (2026). From Skill 1.0 to Skill 2.0: A Modular Skill Middleware
for Research Applications — Evidence from Fixed Income. Working Paper.
github.com/timyefi/skill20-arch
```

---

© 2026 · 作者：叶青 · 文档开源，Skill 源码不开源 · 非商业免费 / 商用需授权 · 「可拆 · 可合 · 可复用」