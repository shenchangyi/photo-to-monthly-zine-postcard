---
name: photo-to-zine-postcard-monthly-variant
status: draft-v0.5
based_on: photo-to-zine-postcard
purpose: 上半保留原图；下半严格复用月历摄影页的空间关系，以自由边缘水彩替换左侧照片。
---

# Photo to Zine Postcard：月历叙事变体 v0.2

## 1. 这版要解决什么

这不是“上半原图 + 下半一张大水彩插画 + 一列文字”。

它必须是：**上半原图 + 下半一张缩小的横向月历摄影页**。下半页的空间关系以参考图为准：左上视觉块、右侧窄月历栏、视觉块下的手写句、大面积留白、最底部横线与三段页脚。区别只在于：左侧视觉块不放另一张原照片，而放从上半原图提取的自由边缘水彩主体。

## 2. 总体画幅与上半区

- 成品：竖版 `3:4`，暖白 / 象牙白纸张，极轻纸纹。`3:4` 是本变体默认比例；它比 `2:3` 更紧凑，能保留摄影明信片的竖版感，同时避免下半月历页出现过长的垂直空洞。
- 上半区是“照片展示容器”，不是固定比例的照片框；其高度与放置方式必须先经过第 2.1 节的原图比例路由。
- 上半原图不得裁切、拉伸、重绘、替换或去除自身已有的边框 / 相机参数 / 水印。
- 常规横图 / 超宽横图时，下半区高度约 `66%–69%`；竖图时下半区可压缩至 `58%–60%`，但下半月历页的左右比例、字级和页脚关系不得改变，只能等比例收紧垂直间距。

### 2.1 原图比例路由（必须在排版前执行）

先计算原图宽高比 `r = width / height`。原图一律使用 `contain`（完整容纳），禁止使用 `cover`（裁切填满）和任何拉伸。外层明信片始终保持 `3:4`。

| 原图条件 | 展示模式 | 上半区规则 |
|---|---|---|
| `r ≥ 1.70` 超宽横图 | 横向摄影条 | 上半容器高 `29%–32%`；原图居中，最大宽度约卡面 `90%`，完整显示。 |
| `1.15 ≤ r < 1.70` 常规横图 | 标准横向照片区 | 上半容器高 `31%–34%`；原图居中，最大宽度约卡面 `88%–92%`。 |
| `0.85 ≤ r < 1.15` 方图 / 近方图 | 实体照片卡 | 上半容器高 `35%–38%`；原图作为居中照片卡，按高度完整容纳，不强行拉满横向宽度。 |
| `0.55 ≤ r < 0.85` 竖图 | 竖向照片票据 | 上半容器高 `40%–42%`；原图作为居中的竖向实体照片，按高度完整容纳，两侧留白必须显得像纸张留边，而不是错误空洞。 |
| `r < 0.55` 极窄竖图 / 长截图 | 需要确认 | 默认不自动生成；询问用户是完整保留，还是只取其中的摄影区域。 |

补充规则：

- 输入若已经包含相机边框、EXIF 参数、品牌字、装饰框或完整摄影版式，默认按“完整摄影成品”处理，整体保留；只有用户明确说“只取内层照片”时才可忽略外层框。
- “完整保留”指保留实际图像，不代表把它硬撑满容器。容器中的剩余纸边是设计留白，不是待填充区域。
- 下半水彩只提取摄影主体（景物、人物、建筑、光线、环境关系），不得提取相机参数、品牌字、界面框、纯色底板或无意义留白。

## 3. 下半区：固定空间关系（最高优先级）

下半区的内部坐标以其自身宽高为基准：

```text
┌──────────────────────────────────────┐
│  左上 70%：自由边缘水彩视觉块  │ 右上：MM │
│  （只占下半区上部，不触及页脚） │     Month │
│                                      │         │
│  水彩下方：手写短句                  │ 右中：书名│
│                                      │       +短引│
│                                      │         │
│  大面积暖白留白                      │ 右下：耳机│
│                                      │       +歌曲│
│──────────────────────────────────────│
│ 作者 / 系列名        日期        收束语 │
└──────────────────────────────────────┘
```

严格尺寸与位置：

- **左上水彩视觉块**：横向占下半区宽度 `66%–70%`；纵向占下半区高度 `50%–54%`；位于下半区的左上，四周保留纸张边距。它要足够大，承接月历页的视觉重量，但仍不得接近页脚。
- **不可犯错**：水彩视觉块不得延伸到下半区底部，不得成为占满下半区的大插画，不得与页脚横线相接，不得做成第二张竖海报。
- **右侧月历栏**：占下半区宽度约 `24%–28%`，从下半区顶部延伸到歌曲区；它必须拥有完整、干净、未被水彩侵入的暖白背景。
- **手写短句行**：仅在水彩视觉块下方、左侧区域内；其基线位于下半区高度约 `58%–62%`，与水彩保持一小段空白。
- **歌曲区**：位于右栏高度约 `72%–76%`，让它承担下半区后段的视觉锚点，不能与手写句处在同一条横线上。
- **留白带**：手写句 / 歌曲区与页脚线之间的纯空白最大为下半区高度 `8%–12%`。留白用于呼吸，不得形成一整块割裂的空洞。
- **页脚**：页脚线位于下半区高度约 `86%–88%`；线下放三段页脚信息，最底边距不超过下半区高度 `6%`。

这套“视觉块—侧栏—手写句—留白—页脚”的节奏，比水彩风格、装饰、文案优先级更高。

## 4. 左上视觉块：自由边缘水彩

### 4.1 主体选择

从上半原图提取最能定义照片的一个完整视觉关系，而不是最容易抠出的物件。

- 山水：云层 + 山脊、水面 + 岸线、树影 + 光线；
- 建筑：建筑轮廓 + 窗影 / 塔吊 / 屋顶 / 光影切面；
- 生活照：人物姿态 + 日常物件 + 环境；
- 日常照：一个具体物体与它所在环境的关系。

### 4.2 绘制规则

- 水彩 + 克制墨线 / 水粉 + 铅笔式编辑插画；保留轮廓、主要结构与原图色彩。
- 视觉块的**空间占位**接近参考图左上照片区，但边缘是自然飞白、干刷、晕染和笔触收边；不要求方形，也不允许显得像裁下来的照片。
- 不得拆成多个小样本、色卡、拼贴块或多组主体。
- 视觉块应有“横向景别”，让右栏与其并列，而不是被它压到下方。

## 5. 右侧月历书签栏（固定参考构图）

右栏不是普通信息流，而是一根独立的“月历书签栏”。它有完整暖白背景，不加分割线、边框或色块；所有元素沿同一条垂直中轴居中，并严格分为“月份锚点 / 文学竖排 / 音乐落款”三组。

### 5.1 月份锚点：右栏顶部

- 大号两位数字置于右栏最上方，是唯一最大字号；英文月份紧随其下并居中。
- 月份数字与英文月份占右栏高度约 `0%–18%`，数字与英文月份之间保留紧凑的 `0.25–0.4em` 间距。
- 日期来源优先级：用户提供拍摄日期 → 可读取的原图 EXIF 拍摄日期 → 留空。不能使用当前日期、文件名日期或模型猜测补全。
- 没有日期时，月份文字留空，但仍保持右栏顶部的留白比例；不得补日期网格。

### 5.2 文学竖排：右栏中段

- 文学组位于右栏高度约 `32%–62%`。书名在右，短引在左，两列均为纵向排版。
- 使用经过联网核验的 `《书名》 + 不超过 20 个汉字的短引`。它们解释照片的内在感受，不逐项说明画面物品；至少贴合场景、情绪、动作 / 想象中的两个维度。
- 书名是主体，必须完整使用《》；短引是相邻说明列。两列间距约 `0.35–0.5em`，不可拉成两根遥远的柱子。
- 禁止伪造书名、作者、名言或出处。找不到可靠引用时，用 `8–16` 字、明确标记为原创的照片旁白，不署书名。

### 5.3 音乐落款：右栏底部

- 音乐组位于右栏高度约 `82%–90%`，与文学组之间保留右栏内最大一段留白。
- 极小耳机图标置于歌曲信息正上方并居中；图标下方居中横排 `歌手《歌曲名》`。图标与歌曲信息绝不并排。
- 不放歌词、平台 Logo、二维码、播放按钮或链接。
- 歌手与歌名必须在可靠页面核验；歌曲情绪至少匹配照片的两个维度。搜不到真正贴切的歌曲时，歌曲区完全留白，不强行填歌。

## 6. 手写短句与页脚

- 手写短句仅放在左上水彩视觉块下方，细、轻、短，不跨入右栏。
- 本变体默认手写短句：`Keep loving, run to mountains and seas.`
- 用户明确提供新短句时，新短句覆盖默认值；否则始终使用默认短句。
- 页脚以一条细横线开始，左 / 中 / 右依次是：作者或系列名、拍摄日期或年份、当期收束语。
- 本变体默认页脚，必须逐字使用：左 `MIXIAN`，中 `2026.08.10`，右 `Free to sway and thrive.`
- 用户明确提供替代信息时才覆盖默认页脚；不能擅自变更拼写、日期或标点。

## 7. 色彩、字体与禁用项

- 月份、书摘、耳机、细线、手写句和页脚使用同一种低饱和深色，从原图情绪主色提取，并确保在暖白纸上可读。
- 设左侧手写短句字号为基准 `1.0`。右侧**书名主竖排必须为 `1.5` 倍**，可在 `1.45–1.55` 内微调；不得更大。
- 右侧短引字号为 `1.0` 倍，歌曲文字为 `0.7–0.75` 倍，页脚为 `0.8–0.9` 倍。除月份数字外，右栏没有任何文字可大于书名。
- 大号月份数字是唯一的最大字号，约为短引字号 `4.0–4.5` 倍；英文月份为短引字号 `1.5` 倍。月份数字与书名不可竞争同一视觉层级。
- 书名用中等字重的优雅衬线，不用粗体；短引字重更轻。书名与短引相邻竖排，间距约 `0.35–0.5em`。
- 数字用高对比衬线，英文月份和页脚用克制衬线，短句用轻盈手写体，中文竖排需清晰。
- 禁止：日期网格、色卡、第二张照片、第二张大插画、满版水彩、logo、徽章、贴纸、波浪涂鸦、长段文字、平台元素、水印。

## 8. 文字策展工作流

1. 识别原图的主体、光线、空间、情绪和主色。
2. 先确定下半水彩的一个完整视觉关系。
3. 有用户要求时，联网检索并核验文学短引与歌曲；优先返回候选搭配供用户选择。
4. 自动生成模式下，只能选用已核验且贴合的搭配；否则触发原创旁白 / 歌曲留空的兜底规则。
5. 再把已经确定的文字数据送入图像生成；禁止在图像生成阶段编造信息。

## 9. 生成提示词骨架

```text
Create a portrait 3:4 Zine postcard on warm ivory paper with a strict upper-photo / lower-monthly-page structure.

Before layout, calculate the supplied image aspect ratio r = width / height. The outer postcard always stays portrait 3:4. Use contain only: never crop, use cover, stretch, repaint, replace, or remove any existing detail from the supplied photo. If the input already contains a camera frame, EXIF, brand text, decorative frame, or an existing photo-card design, preserve the whole supplied image as one finished photographic artifact unless the user explicitly asks to use only the inner photo.

Route the upper photo display by r:
- r >= 1.70: use a horizontal photographic strip, 29–32% of card height, centered, maximum width about 90% of card width.
- 1.15 <= r < 1.70: use a standard horizontal photo area, 31–34% of card height, centered, maximum width 88–92% of card width.
- 0.85 <= r < 1.15: use a centered square-photo card, 35–38% of card height, fitted completely by height without forcing it to fill the width.
- 0.55 <= r < 0.85: use a centered vertical-photo ticket, 40–42% of card height, fitted completely by height. The paper margins on both sides must look intentional and editorial, never like a missing or failed image.
- r < 0.55: do not generate automatically; ask whether the whole tall image or only its photographic area should be retained.

Below the selected photo display, compose a miniature horizontal monthly photography page, not a large vertical illustration. For wide and standard landscape source photos, the lower page is 66–69% of total card height. For square sources it is 62–65%; for portrait sources it is 58–60%. In shorter lower pages, compress only vertical gaps by up to 15%; do not shrink or change the left/right proportions, type scale, or footer hierarchy.
- In the lower page's upper-left 66–70% width and 50–54% height, place ONE source-specific watercolor-and-ink visual block. It must have free organic watercolor edges and remain clearly separated from the footer.
- The watercolor block may extract only the scene, subject, light, and spatial relationship from the source photo. Never reproduce EXIF text, brand lettering, UI chrome, photo frames, blank backdrop, or other non-photographic packaging inside the watercolor.
- In the lower page's right 24–28% width, keep an uninterrupted warm-paper bookmark column with no divider or border. Center all groups on one vertical axis. At column height 0–18%, set “{month_number}” and “{english_month}”. At height 32–62%, set the verified vertical literary block: book title “《{book_title}》” on the right and “{quote_or_original_caption}” on the left, with 0.35–0.5em between them. At height 82–90%, place a tiny headphone icon centered ABOVE the horizontally centered “{artist}《{song_title}》”.
- Under the left watercolor block, around lower-page height 58–62%, set the exact handwritten line “{handwritten_line}”. Default: “Keep loving, run to mountains and seas.”
- Keep the literary block and music group separated by the right column's largest intentional blank interval. Limit the pure blank band before the footer line to 8–12% of lower-page height.
- At lower-page height 86–88%, draw one thin horizontal rule; below it, set exact footer text left “{author}”, center “{date}”, right “{closing_line}”. Default exactly: left “MIXIAN”, center “2026.08.10”, right “Free to sway and thrive.”

Typography: treat the left handwritten line and quote as 1.0. Set the book-title vertical line to exactly 1.5x that size; song 0.7–0.75x; footer 0.8–0.9x; English month 1.5x. The month number is the only larger display type at 4.0–4.5x the quote. No right-column text except the month number may exceed the book-title size.

Use one legible muted dark text color sampled from the photo. Do not add a date grid, swatches, multiple motifs, palette strips, logos, badges, platform controls, watermarks, or extra text. Never let the watercolor fill the lower page or reach the footer.
```

## 10. 输出前检查

- [ ] 已在排版前计算 `r = width / height`，并按比例路由选择了上半图片区的展示模式与高度。
- [ ] 上半原图使用 `contain` 完整容纳：没有裁切、拉伸或 `cover` 填充；带相机框、EXIF、品牌字或装饰框的输入，整体原样保留（除非用户明确要求只取内层照片）。
- [ ] 下半水彩只提取摄影主体与场景关系，不复制原图中的 EXIF、品牌、界面框或外层底板。
- [ ] 上半是未改写的实际原图。
- [ ] 下半不是一张大水彩插画，而是缩小横向月历页。
- [ ] 成品比例为 3:4；水彩位于下半左上，仅占左侧约 70% 和下半高度约 50%。对于方图或竖图，下半仅压缩垂直间距，不牺牲右栏、字级和页脚关系。
- [ ] 右栏与水彩并列，有完整暖白背景、月份锚点、书摘、歌曲区。
- [ ] 水彩下有手写句位；歌曲位于更靠下的右栏；留白带不超过下半高度 12%，页脚紧凑地沉在最底部。
- [ ] 书名字号 = 左侧手写句 1.5 倍；短引、歌曲、页脚均更小；只有月份数字更大。
- [ ] 页脚横线与三段信息独立于水彩，不被任何画面触碰。
- [ ] 日期、书摘、歌曲、署名均已提供 / 核验，或已按兜底规则留空。
