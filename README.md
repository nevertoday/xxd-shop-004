<div align="center">

# 🦁 XXD Shop 004｜烘焙系列海报

### 够大、够近、够好吃，一套上新一个品牌世界

<strong>简体中文</strong> · <a href="README.en.md">English</a>

</div>

> 原始提示词：[简体中文原文](references/original-prompt/zh-CN.md) · [English](references/original-prompt/en.md)

## 样张

暂无样张。下文命令只是用法示例，不是视觉证据。

## 它解决什么

烘焙店上新，最常见的两种失败：一种是每张图都好看，放在一起却像四家店；另一种是一套图统一了，结果每张都是同一个模板换个面包。

**Shop 004** 用原稿的一句话解决：**不同的海报可以换构图，但字体气质、色彩情绪和品牌识别要共享。** 做系列时，先出一张定调海报给你确认，之后每款产品都参考它的“气质”，构图各自重新找。

单张也一样能做：产品够大够近，酥皮、气孔、拉丝、流心、糖霜这些最馋的质感被放大，光线像清晨的烘焙橱窗。

## 系列怎么做

1. 你给一组产品（多张图、一个目录或几个产品名）。
2. 先出第一款的定调海报，你确认字体、颜色和店名的感觉。
3. 其余每款各出一张：继承定调图的字体气质、色彩情绪和品牌识别，构图换新的，比如巨字做背景、竖向堆叠、单个超大产品、多件错落。

不满意定调图，就只重做定调图，后面的不会跟着错。

## 你需要准备

- **产品图或产品名：** 有图时切面和馅料以图为准，不会加料。
- **店名或品牌字标：** 做系列时强烈推荐，它是整套的识别。
- **事实：** 价格、“每日现做”、获奖、开店年份，用 `--facts` 或描述说明；没说的不会出现。

## 快速判断

| 你关心的问题 | 回答 |
|---|---|
| **你会得到什么** | 一张或一套明快、诱人、有字体记忆点的烘焙电商海报 |
| **一眼可辨的特点** | 超大近景产品 · 暖亮晨光 · 产品名是品牌图形 · 杂志式手写标注 · 系列构图各不相同 |
| **适合什么商品** | 面包、蛋糕、可颂、挞派、饼干、月饼等烘焙；其他品类推荐 001 或 009 |

## 开始使用

```bash
git clone https://github.com/nevertoday/xxd-shop-004.git
ln -s "$(pwd)/xxd-shop-004" ~/.claude/skills/xxd-shop-004
```

```text
# 一张：可颂单品海报
/xxd-shop-004 ./开心果可颂.jpg --product "开心果流心可颂" --size 3:4 --text prompt --locale zh-CN

# 一套：目录里四款新品，先定调再出其余三张
/xxd-shop-004 ~/Desktop/秋季上新/ --product "麦野烘焙 · 秋季上新" --size 3:4 --text prompt --locale zh-CN

# 只有产品名的系列
/xxd-shop-004 --product "巴斯克芝士蛋糕；伯爵红茶戚风；海盐焦糖布朗尼" --size 4:5 --text prompt --locale zh-CN
```

常用参数：`--product` · `--size` · `--text prompt / exact / plan / none` · `--facts` · `--locale`。完整参数见[家族运行合同](references/shop-runtime.md)。

## 边界与信任

- 原始提示词逐字保存，是唯一的审美权威。
- 系列只共享原稿点名的三项：字体气质、色彩情绪、品牌识别，构图、产品和文案不会从上一张复制。
- 交付 PNG 位图；每次调用都新建任务目录。

<!-- xxd-shop-tail -->
## 项目结构

```text
xxd-shop-004/
├── SKILL.md
├── README.md / README.en.md
├── LICENSE
├── agents/openai.yaml
├── assets/examples/
├── scripts/
│   ├── configured_imagegen.py
│   └── shop_preferences.py
└── references/
    ├── shop-runtime.md
    ├── runtime-preferences.md
    ├── sample-workflow.md
    └── original-prompt/
        ├── README.md
        ├── zh-CN.md
        └── en.md
```

<!-- xxd-readme-ads:start -->
## 关于 XXD

XXD 是小小东品牌名的缩写，本项目由小小东创建并维护：[@xiaoxiaodong01](https://x.com/xiaoxiaodong01)。

## 小小东多端会员 · 699 元/年

> **广告与商业信息声明：** 以下二维码、会员与付费服务链接属于小小东的广告信息。是否扫码或购买完全自愿，不影响本开源项目的访问与使用。

一次年费，同时开通三项会员权益：**知识星球 + 小小东成员提示词库 + 全部 将军总指挥 Skills 会员**。三项权益合并在同一份会员中，无需分别购买。

<!-- xxd-shop-command-system:start -->

### Skills 如何协作

| 层级 | 包含内容 | 用途 |
|---|---|---|
| **General** | `xxd-shop-all` | 识别可用的编号 Skills，按商品、用途和画面需求推荐，并组织多风格试稿与批量任务。 |
| **Soldier** | `xxd-shop-NNN` | 每个编号执行自己的原始提示词与审美，完成 General 分派的具体任务。 |

<!-- xxd-shop-command-system:end -->

### 会员权益

1. **微信一对一 AI 学习与项目答疑**
   扫描下方二维码，添加小小东微信，围绕 AI 学习、工具使用和实际项目进行一对一沟通，获得答疑与建议；代表性问题将整理为会员内容。
2. **持续更新的成员提示词库**
   [小小东成员提示词库](https://vip.xiaoxiaodong.ai/)当前约有 3.2 万条提示词，会持续整理和扩充，目标超过 10 万条。
3. **全部 将军总指挥 Skills 与使用答疑**
   一份会员覆盖全部 将军总指挥 Skills；使用过程中遇到问题，可以获得相应的使用说明与答疑。
4. **高频刚需优先处理**
   会员提出的高频、刚需提示词与 Skills 需求，会优先评估和开发。

### 如何开通

- 可在[成员网站](https://vip.xiaoxiaodong.ai/)自助开通。
- 也可以扫描下方二维码，添加小小东微信，进行一对一沟通并获得开通协助。

<p align="center"><a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="联系小小东" width="280"></a></p>
<!-- xxd-readme-ads:end -->

## 许可证

本项目（包括 Skill、提示词、脚本、文档及随附样张）采用 **PolyForm Noncommercial License 1.0.0**。完整法律条文请见 [LICENSE](LICENSE)，官方页面见 <https://polyformproject.org/licenses/noncommercial/1.0.0>。

用人话说：

- 个人可以用于学习、研究、实验、测试、兴趣项目和私人娱乐；慈善机构、教育机构、公共研究/安全/卫生机构、环保组织及政府机构也可以使用。
- 在**非商业目的**下，你可以使用、复制、修改、制作衍生作品并分享；分享时必须同时提供本许可证（或上面的链接）以及作者提供的所有 `Required Notice:` 声明。
- 不允许用于商业产品或服务、收费交付、出售访问权或许可，或任何预期会带来商业应用的用途。需要商业使用时，请先向版权方另行取得书面许可。
- 本协议只授予其中明确写出的著作权许可和有限的专利许可，不授予商标、品牌名称或其他未明确授予的权利，也不能把你的许可再转授给他人。
- 如果收到书面违约通知，须在 32 天内纠正并采取实际补救措施，否则许可会立即终止；就专利侵权提出书面主张也会终止专利许可。
- 内容按“现状”提供，在法律允许的范围内不作任何担保，使用风险和可能的损失由使用者自行承担。
