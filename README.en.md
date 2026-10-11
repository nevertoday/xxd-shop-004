<div align="center">

# 🦁 XXD Shop 004 | Bakery Series Posters

### Big, close, delicious — one launch, one brand world

<a href="README.md">简体中文</a> · <strong>English</strong>

</div>

> Original brief: [Simplified Chinese original](references/original-prompt/zh-CN.md) · [English reading translation](references/original-prompt/en.md)

## Samples

No samples yet. The commands below are usage examples, not visual evidence.

## What it solves

Bakery launches usually fail one of two ways: every poster is lovely but together they look like four different shops, or the set is consistent because it is one template with the pastry swapped.

**Shop 004** follows one line of its brief: **layouts may change from poster to poster, but type character, colour mood and brand identity are shared.** For a series it first makes one anchor poster for your approval; every following product inherits that character and finds its own composition — giant type as background structure, a vertical stack, one oversized product, a staggered group.

Single posters work too: the product is big and close, with flaky layers, open crumb, cheese pull, molten centres and glaze amplified under bright morning-window light.

## How a series runs

1. Give a set of products — several photos, a folder, or several names.
2. Approve the anchor poster for the first product.
3. Each remaining product gets its own poster referencing its own photo plus the approved anchor; only the three shared qualities carry over.

## Getting started

```bash
git clone https://github.com/nevertoday/xxd-shop-004.git
ln -s "$(pwd)/xxd-shop-004" ~/.claude/skills/xxd-shop-004
```

```text
/xxd-shop-004 ./pistachio-croissant.jpg --product "Molten Pistachio Croissant" --size 3:4 --text prompt --locale en-US
/xxd-shop-004 ~/Desktop/autumn-launch/ --product "Maiye Bakery · Autumn Launch" --size 3:4 --text prompt --locale zh-CN
```

Key flags: `--product`, `--size`, `--text prompt / exact / plan / none`, `--facts`, `--locale`. Full list in the [family runtime](references/shop-runtime.md).

## Boundaries

- The original brief is kept verbatim and is the only aesthetic authority.
- Cross-sections and fillings follow your photo; nothing is added.
- Sales, awards, years, "baked daily" and "limited" appear only when you provide them.
- Bakery only; other categories are pointed to Shop 001 or 009.

<!-- xxd-shop-tail -->
## Project structure

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
## About XXD

XXD is Xiaoxiaodong's abbreviated brand name. This project is created and maintained by [@xiaoxiaodong01](https://x.com/xiaoxiaodong01).

## Xiaoxiaodong multi-platform membership · CNY 699/year

> **Advertising disclosure:** The QR code, membership, and paid-service links below are XXD promotional information. Scanning or purchasing is entirely optional and does not affect access to this open-source project.

One annual membership unlocks three benefits together: **Knowledge Planet + the XXD Member Prompt Library + membership for all General Skills**. They are included in one membership; no separate purchase is required.

<!-- xxd-shop-command-system:start -->

### How the Skills work together

| Level | Included | What it does |
|---|---|---|
| **General** | `xxd-shop-all` | Detects available numbered Skills, recommends them by product, placement and visual need, and organizes multi-style and batch tasks. |
| **Soldier** | `xxd-shop-NNN` | Each numbered Skill follows its own original brief and aesthetic to complete the specific task assigned by the General. |

<!-- xxd-shop-command-system:end -->

### What you receive

1. **One-to-one WeChat AI learning and project support**
   Add Xiaoxiaodong on WeChat via the QR code below to discuss AI learning, tools, and real projects one to one, with practical guidance and answers. Representative questions may be organized into member resources.
2. **A growing member prompt library**
   The [XXD Member Prompt Library](https://vip.xiaoxiaodong.ai/) currently contains about 32,000 prompts and will keep expanding, with a goal of exceeding 100,000.
3. **All General Skills and usage support**
   One membership covers every General Skill, with usage guidance and Q&A when you need help.
4. **Priority for high-need requests**
   Frequently requested, high-need prompts and Skills are reviewed and developed first where appropriate.

### How to join

- [Activate membership on the member website](https://vip.xiaoxiaodong.ai/).
- Or scan the QR code below to add Xiaoxiaodong on WeChat for one-to-one activation support.

<p align="center"><a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="Contact Xiaoxiaodong" width="280"></a></p>
<!-- xxd-readme-ads:end -->

## License

This project—including its Skill, prompts, scripts, documentation, and accompanying samples—is released under the **PolyForm Noncommercial License 1.0.0**. The complete legal text is in [LICENSE](LICENSE); the official page is <https://polyformproject.org/licenses/noncommercial/1.0.0>.

In plain language:

- You may use it for personal study, research, experiments, testing, hobbies, and private entertainment. Charities, educational institutions, public research/safety/health organisations, environmental-protection organisations, and government institutions may also use it.
- For **noncommercial purposes**, you may use, copy, modify, create derivative works, and share the project. When sharing, include this license (or the link above) and every `Required Notice:` line supplied by the author.
- Commercial products or services, paid delivery, selling access or licenses, and uses with an anticipated commercial application are not allowed. Obtain separate written permission from the copyright holder for commercial use.
- The license grants only the stated copyright and limited patent rights. It grants no trademark, brand, or other unstated rights, and you may not sublicense or transfer your license.
- If you receive written notice of a violation, you have 32 days to come into full compliance and take practical corrective steps; otherwise the licenses end. A written patent-infringement claim also ends the patent license.
- The project is provided **as is**, without warranties, and you accept the risks and any resulting liability to the extent permitted by law.
