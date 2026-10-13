# XXD Shop 004 样张

每张都是本编号按 `references/sample-workflow.md` 一次生成、目视通过的原图，像素未改，只清理了元数据。商品是虚构的演示品牌，画面上的价格、规格等数字都是演示设定。

| 文件 | 用途 | 实际像素 | 输入 | 文字方式 | visual_review |
|---|---|---|---|---|---|
| `c01-category-3x4-1086x1448.png` | 上新海报 | 1086x1448 | Logo `logo-maiyu.png` | plan zh-CN | passed |
| `c02-category-1x1-1254x1254.png` | 上新主图 | 1254x1254 | Logo `logo-maiyu.png` | plan zh-CN | passed |
| `c03-category-4x5-1122x1402.png` | 社媒 | 1122x1402 | Logo `logo-maiyu.png` | plan zh-CN | passed |
| `c04-category-9x16-941x1672.png` | 门店竖屏 | 941x1672 | Logo `logo-maiyu.png` | plan zh-CN | passed |
| `c05-category-1x1-1254x1254.png` | 上新主图 | 1254x1254 | Logo `logo-maiyu.png` | plan zh-CN | passed |
| `c06-category-16x9-1672x941.png` | 横幅 | 1672x941 | 商品图 `product-maiyu-cookies.jpg`、Logo `logo-maiyu.png` | plan zh-CN | passed |
| `p01-set-3x4-1086x1448.png` | 系列上新海报 | 1086x1448 | 原图 `croissant.jpg`、Logo `logo-maiyu.png` | prompt zh-CN | passed |
| `p02-set-3x4-1086x1448.png` | 系列上新海报 | 1086x1448 | Logo `logo-maiyu.png` | prompt zh-CN | passed |
| `p03-set-3x4-1086x1448.png` | 系列上新海报 | 1086x1448 | Logo `logo-maiyu.png` | prompt zh-CN | passed |
| `s01-size-1x1-1254x1254.png` | 上新主图 | 1254x1254 | 原图 `croissant.jpg`、Logo `logo-maiyu.png` | prompt zh-CN | passed |
| `s02-size-3x4-1086x1448.png` | 上新海报 | 1086x1448 | 原图 `croissant.jpg`、Logo `logo-maiyu.png` | prompt zh-CN | passed |
| `s03-size-9x16-941x1672.png` | 门店竖屏 | 941x1672 | 原图 `croissant.jpg`、Logo `logo-maiyu.png` | prompt zh-CN | passed |
| `s04-size-16x9-1672x941.png` | 横幅 | 1672x941 | 原图 `croissant.jpg`、Logo `logo-maiyu.png` | prompt zh-CN | passed |
| `s08-special-4x5-1122x1402.png` | 上新海报 | 1122x1402 | 原图 `croissant.jpg`、Logo `logo-maiyu.png` | prompt en-US | passed |

## 输入素材

`sources/` 里是生成时交给本编号的输入缩样，模拟商家手里的素材：带包装与 Logo 的商品图、品牌 Logo，个别为原图。
演示品牌、Logo 和商品图由本项目生成；其中以 Unsplash 照片为底的，署名如下，适用 [Unsplash License](https://unsplash.com/license)，**不属于**本仓库的 PolyForm Noncommercial 授权范围。

| 输入 | 说明 · 来源 |
|---|---|
| `sources/croissant.jpg` | 原图 [VzUE5RtCuBA](https://unsplash.com/photos/VzUE5RtCuBA) · @personal_graphic |
| `sources/logo-maiyu.png` | 演示品牌 Logo，本项目生成 |
| `sources/product-maiyu-cookies.jpg` | 演示商品图，本项目生成 |
