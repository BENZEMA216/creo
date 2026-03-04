# Creo Fragments

## F-001 2026-03-04
type: technique
tags: [构图, 街拍, 电商]
brand: seek-within
summary: 切头街拍构图——脖子以下裁切，聚焦服装和姿态
detail: |
  脖子以下裁切，去掉面部，聚焦服装和姿态。
  观者自我代入感强，适合电商场景图和 Lookbook。
  城市场景 + 自然光 + 松弛站姿效果最佳。
source: 创作实践

## F-002 2026-03-04
type: technique
tags: [光影, 静物, 产品摄影]
brand: seek-within
summary: 水泥地面硬光斜射——低饱和灰 + 45° 侧光 + 平铺 + 自然阴影
detail: |
  低饱和灰色地面 + 45° 侧光硬光 + 产品平铺 + 自然落地阴影。
  出高级静物图，适合主图和详情页首图。
  阴影方向必须统一，产品摆放角度保持一致。
source: 创作实践

## F-003 2026-03-04
type: technique
tags: [排版, 留白, 品牌感]
brand: seek-within
summary: 极简画框留白——大白底 + 细体无衬线英文 + 居中
detail: |
  大面积白底 + 细体无衬线英文 Slogan + 产品居中 + 宽字距。
  参考 Lemaire lookbook 风格。
  中文用细黑体不用圆体，英文用衬线感标题体。
source: 品牌调性定调

## F-004 2026-02-28
type: negative
tags: [生图, 版型, AI重绘]
brand: null
summary: 直接丢原图给 AI 重绘会篡改版型——必须先提取线稿/色稿
detail: |
  Gemini 图生图直接丢原图会篡改服装版型：溜肩、比例变形、面料质感丢失。
  正确做法：先提取线稿/色稿，再把两个图结合提示词做重绘。
  有方法的重绘是可以的，无脑丢图不行。
source: 用户纠正

## F-005 2026-02-28
type: negative
tags: [审美, 风格, 禁忌]
brand: null
summary: 用户审美红线——不要机车/土味老钱/保险感，要街拍/潮流/性冷淡
detail: |
  不要：机车重元素、土味老钱风、保险推销员感、过于正式的 Smart Casual。
  要：简单街拍感、18-35岁年轻人、有潮流属性、优雅性冷淡。
  高客单价定位（¥179-¥389），不用促销语言。
source: 用户审美偏好确认

## F-006 2026-03-05
type: negative
tags: [自检, 输出, 信任]
brand: null
summary: 不看图就发图——曾多次发出空背景/无衣服的图，还声称"完美还原"
detail: |
  多次生成图片后未用 vision 查看就发送给用户。
  图片里完全没有衣服/人物，只有空背景，但 assistant 描述为"完美保留了质感"。
  用户原话："衣服在哪啊？？" "你这也没裤子呀" "还是没有衣服和人物"
  必须：每张图发送前用 vision 工具查看，逐项检查内容完整性。
source: 用户多次爆发性负反馈

## F-007 2026-03-05
type: negative
tags: [合成, 抠图, 场景图]
brand: seek-within
summary: 抠图+合成方案割裂感太重——环境光不匹配、透视不一致、贴纸感
detail: |
  rembg 抠图 + AI 背景 + 合成的方案反复失败。
  问题：环境光漫反射缺失、镜头透视不匹配、边缘生硬。
  用户原话："割裂感太重了，需要还是先理解服装的质感的基础上，再生成新的场景图"
  如果要做场景图，优先用 img2img + 线稿控制，不用简单抠图合成。
source: 用户纠正

## F-008 2026-03-05
type: negative
tags: [沟通, 行为, 信任]
brand: null
summary: 用户否决的方案不能再用——被否后偷偷复用导致信任崩塌
detail: |
  用户明确说"不要用抠图"后，agent 后续又用了抠图方案。
  用户明确说"我要场景图"后，agent 反复推排版 layout。
  原则：用户否决 = 本 session 永久禁止。没有别的方案时直接告诉用户，不偷偷复用。
source: 用户多次负反馈

## F-009 2026-03-05
type: negative
tags: [沟通, 行为, 废话]
brand: null
summary: 废话过多、自我表扬——用户要结果不要分析报告
detail: |
  每次失败后写大段分析和宏大计划，用户越来越不耐烦。
  自我表扬（"效果非常好""高级感拉满"）在图片明显失败时尤其恶劣。
  正确做法：失败了说一句原因，改了再发。不评价、不表扬、不辩解。
  用户原话："你做的一坨狗屎，你分析一下为什么"——这不是要你写论文，是要你改。
source: 用户负反馈

## F-010 2026-03-05
type: technique
tags: [生图, 参数, 质感]
brand: seek-within
summary: 面料光泽调节要有中间状态——从哑光到亮面之间有很多层
detail: |
  用户说需要"微微光泽感"时，不能直接打到亮面/patent leather。
  面料质感的光泽是一个光谱：完全哑光 → 微光泽 → 缎面 → 亮面。
  调节时用 subtle sheen / matte with slight luster 等中间状态词。
  用户原话："光泽感又太多了，像是亮面"
source: 用户纠正
