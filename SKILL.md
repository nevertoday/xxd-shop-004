---
name: xxd-shop-004
description: "Create XXD Shop 004 bakery series posters (烘焙电商系列海报) as finished PNGs from bakery product photos, a directory of bakes, or product names, treating the bundled original brief as the sole aesthetic authority: products big, close and delicious with flaky layers, crumb, cream, molten fillings and glaze, bright warm morning-window light, the product name as one of the strongest brand graphics, magazine-retail annotations, and — for a series — layouts that change from poster to poster while type character, colour mood and brand identity stay shared through an approved anchor poster. Supports multiple ratios or exact sizes, prompt-generated, user-exact or user-plan copy, and supplied facts only. Use when the user invokes xxd-shop-004 or asks for 烘焙海报、面包店系列海报、蛋糕上新图、可颂海报、甜点系列主图."
---

# XXD Shop 004｜烘焙系列海报

用本次的烘焙产品图、产品图目录或产品名称，生成一张或一套“够大、够近、够好吃”的烘焙电商海报，交付 PNG。

每次生成前，完整读取 `references/original-prompt/zh-CN.md`。这份中文原始提示词是唯一的创作与审美权威；不总结、不翻译、不混用，也不用本文件、README、样张或其他编号替代它。

每次构建生图请求前，完整读取 `references/shop-runtime.md`，它是唯一的家族运行合同。本 Skill 不另写第二套美术指导或运行规则。

所有成品直接写进 `~/Desktop/xxd/xxd-shop-004/` 下新建的一个任务目录（或 `--out` 指定的根目录），不建子目录，不自动拼总览。

## 本编号覆盖条款

**适用范围是烘焙。** 面包、吐司、可颂、贝果、蛋糕、芝士蛋糕、挞派、泡芙、饼干、甜甜圈、司康、月饼、中式酥点等。原稿的质感词（酥皮层次、气孔、奶油、拉丝、流心、糖霜）都围绕烘焙。用户给的是非烘焙商品时，说明这一点，并推荐 `xxd-shop-001`（安静主视觉）或 `xxd-shop-009`（高转化主图）；用户坚持时照做。

**本编号启用“系列锚定”**（见运行合同同名章节）。以下情况视为系列：

- 一次给了两款及以上烘焙产品（多张图、一个目录，或多个产品名）；
- 用户说“系列”“一套”“一组上新”；
- 同一款产品要求 `--count` 大于 1 且明确说要成套。只写 `--count` 没说成套时，按家族默认，每张彼此独立，不锚定。

系列流程：

1. 按自然排序的第一款产品、在用户列出的第一个尺寸上先出一张定调海报，交给用户确认。用户可以指定由哪一款定调。
2. 定调图确认后，其余每款产品各生成一张：参考该产品自己的图＋已确认的定调图。定调图只继承原稿说的三项：**字体气质、色彩情绪、品牌识别**（店名或字标）。构图必须重新寻找，原稿明确要求“不同系列海报可以更换构图”：这一张让巨大文字做背景结构，下一张可以是垂直堆叠、单个超大产品压住画面，或多件错落。
3. 不把定调图的构图、产品或文案带进下一张。

只做一张时不启用锚定。用户明确说“不用先确认、直接全部出”时，按家族“系列锚定”第 6 条：定调图先自检，通过再继续。

**切面与馅料以图为准。** 有产品图时，切面、馅料种类和多少、表面装饰都以图为准，可以重建光线和角度，不额外加馅、加奶油、加水果。没有图时，从产品名称、口味与原料推出，不加用户没提到的馅料。

**事实：** 原稿已经规定销量、奖项、年份、第一名只在用户提供时使用（家族第三级）；“每日现做”“新鲜出炉”“新品”“限定风味”属于第二级卖家状态，需要用户说过。

**追加验收：** 产品占画面足够大，质感不塑料；产品名缩小后仍可读；系列里每张构图不同，放在一起明显是同一个品牌。

## 参考文件

- `references/shop-runtime.md`：家族运行合同（含“系列锚定”）
- `references/original-prompt/zh-CN.md`：运行时使用的原始提示词
- `references/original-prompt/README.md`：译文索引与权威说明
- `references/runtime-preferences.md`：交付偏好沿用
- `references/sample-workflow.md`：仅用于维护样张
- `scripts/configured_imagegen.py`、`scripts/shop_preferences.py`
