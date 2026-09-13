# random

随手做的一些小实验。**在线阅读:<https://ktmud.github.io/random/>**(GitHub Pages)

## 🧮 数学难题时间线 · 人类与 AI

**首页:<https://ktmud.github.io/random/>**

按时间线梳理 2023–2026 年被攻克的重要数学难题,每张卡片标注 🧑 人类 / 🤖 AI / 🤝 人机合作。人类一侧(爱因斯坦瓷砖、几何朗兰兹、移动沙发、三维挂谷、希尔伯特第六问题、解结数、渗流锐利性猜想、2026 菲尔兹奖等)链接到原始报道或论文;AI 参与的每个问题有一页详解,向大众讲清来龙去脉以及 AI 到底是怎么证明(或推翻)它的。

AI 参与的详解页:

| 时间 | 事件 | 页面 |
|---|---|---|
| 2023-12 | FunSearch 与帽子集问题:LLM 第一次「发现」新数学 | [`problems/cap-set.html`](problems/cap-set.html) |
| 2024-07 → 2025-07 | 国际数学奥林匹克:AI 从银牌到金牌 | [`problems/imo.html`](problems/imo.html) |
| 2025-05 | AlphaEvolve:4×4 矩阵乘法 48 次、11 维亲吻数 593 | [`problems/alphaevolve.html`](problems/alphaevolve.html) |
| 2025-08 → 10 | 「解决十个 Erdős 问题」乌龙:文献检索 ≠ 解决 | [`problems/erdos-literature.html`](problems/erdos-literature.html) |
| 2025-12 | Aletheia 一周扫过 700 个 Erdős 公开问题 | [`problems/aletheia.html`](problems/aletheia.html) |
| 2026-01 | Erdős 第 728 号:第一个被 AI 独立解决的 Erdős 问题 | [`problems/erdos-first.html`](problems/erdos-first.html) |
| 2026-02 → 07 | First Proof:用「从未发表」的题目给 AI 出考卷 | [`problems/first-proof.html`](problems/first-proof.html) |
| 2026-05-20 | 单位距离猜想被推翻(Erdős,1946) | [`problems/unit-distance.html`](problems/unit-distance.html) |
| 2026-05-21 | AlphaProof Nexus:9 个 Erdős 问题、44 个 OEIS 猜想 | [`problems/alphaproof-nexus.html`](problems/alphaproof-nexus.html) |
| 2026-08-01 | Astra:第一个非 sofic 群(Gromov,1999)及署名争议 | [`problems/non-sofic.html`](problems/non-sofic.html) |
| 2026-09-08 | 纳维–斯托克斯方程:千禧年难题的有限时间爆破与署名风波 | [`problems/navier-stokes.html`](problems/navier-stokes.html) |

### 里面有什么

- 首页:读前须知(「解决」还是「查到」/ 谁来检查证明 / 功劳算谁的)+ 按「解决者 × 类型」两组筛选的时间线 + 单位距离动画
- 每个详解页:问题是什么 → 为什么难 → AI 做了什么(听得懂的证明思路)→ 争议与意义 → 延伸阅读
- 三个小交互:3×3 帽子集小游戏、方格点阵里的单位距离计数、纳维–斯托克斯跨尺度级联示意动画

### 技术说明

- 纯静态 HTML,零依赖、无构建;样式在 [`assets/site.css`](assets/site.css),与挂谷猜想页同一套配色
- 时间线只收录有公开论文或形式化证明可查的事件;署名与数据使用的争议只转述各方公开说法
- 信息截至 2026 年 9 月中旬,部分结果尚待同行评审

## 🪡 一根针的百年难题 —— 挂谷猜想可视化

**在线阅读:<https://ktmud.github.io/random/kakeya/>**

用可交互的动画,给普通读者讲清**挂谷猜想**(Kakeya Conjecture):
从 1917 年挂谷宗一「一根针如何调头」的小谜题,讲到贝西科维奇「面积可以任意小」的反直觉构造、
「零面积却满维度」的现代猜想,以及王虹与 Joshua Zahl 的 2025 年三维证明和 2026 年菲尔兹奖。

![页面预览](kakeya/preview.png)

### 里面有什么

- **四块场地,同一根针** —— 圆 / 勒洛三角形 / 等边三角形 / 三尖摆线内的连续转针动画(同比例绘制,面积对比)
- **佩龙树** —— 切碎、平移、叠放:面积被一步步「折叠」掉,任意方向的针却都还在(面积由页面逐像素实测)
- **帕尔的戏法** —— 「斜一点、绕远路」,平移一根针几乎不花面积
- **接力调头** —— 佩龙树 + 帕尔机动合体:针在 8 根细条间接力转完整个扇区,扫过面积随偏角 δ 减小而下降
- **四份拷贝拼满 180°** —— 方向表盘 + 四份旋转拷贝轮流「值班」,补全调头路线的最后一步
- **数格子量维度** —— 盒计数演示:线段 ≈ 1 维、方块 ≈ 2 维、贝西科维奇式集合 ≈ 2 维(虽然面积趋于零)
- **三维针丛** —— 可拖拽旋转的三维挂谷集示意
- 里程碑时间线:1917 → 2025 证明 → 2026 菲尔兹奖

### 技术说明

- 单文件 `kakeya/index.html`,零依赖、无构建,纯 Canvas + 原生 JS
- 三尖摆线中针的运动采用精确的切线弦参数化(针长恒等于 1,误差 ~10⁻¹⁶,发布前经数值验证)
- 等边三角形取高 = 针长,是帕尔定理的临界情形;顶点旋转的可用长度恰好为 1
- 佩龙树为简化版构造(每层右半部分左移固定比例,α = 0.42 为数值实验最优),面积为实时逐像素测量

### 延伸阅读

- Wang & Zahl, [*Volume estimates for unions of convex sets, and the Kakeya set conjecture in three dimensions*](https://arxiv.org/abs/2502.17655) (2025)
- Terence Tao, [*The three-dimensional Kakeya conjecture, after Wang and Zahl*](https://terrytao.wordpress.com/2025/02/25/the-three-dimensional-kakeya-conjecture-after-wang-and-zahl/)
- Quanta Magazine, [*"Once in a Century" Proof Settles Math's Kakeya Conjecture*](https://www.quantamagazine.org/once-in-a-century-proof-settles-maths-kakeya-conjecture-20250314/)
- Quanta Magazine, [*Hong Wang Wins 2026 Fields Medal*](https://www.quantamagazine.org/hong-wang-wins-2026-fields-medal-the-third-woman-ever-20260723/)

---

*页面由 [Claude Code](https://claude.ai/code) 生成。*
