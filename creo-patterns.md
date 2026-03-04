# Creo Patterns

## P-001 水泥光影静物风
tags: [静物, 产品摄影, 高级感]
features:
  - 低饱和灰色背景（水泥/石材质感）
  - 45° 侧光硬光，自然落地阴影
  - 产品平铺或 45° 俯拍
  - 极简背景，无多余道具
  - 阴影方向统一
use_when: 产品主图、详情页首图、品牌画册单品页
fragments: [F-002]
prompt_template: |
  product flat lay on concrete surface, low saturation gray,
  hard directional light from 45 degrees left, natural drop shadow,
  minimal background, high-end editorial style
avoid:
  - 阴影方向不一致
  - 背景饱和度过高
  - 道具喧宾夺主

## P-002 切头街拍风 (Headless Street Style)
tags: [街拍, 电商, 场景图]
features:
  - 脖子以下裁切，无面部
  - 城市场景（咖啡馆/美术馆/街头）
  - 自然光或柔和环境光
  - 松弛站姿，无刻意摆拍感
  - 服装是绝对主角
use_when: 电商场景图、社媒素材、Lookbook
fragments: [F-001]
prompt_template: |
  headless street style photo, cropped below neck,
  urban setting, natural lighting, relaxed pose,
  focus on clothing details and silhouette
avoid:
  - 合成时光影方向与背景不一致
  - 人物比例失真
  - 过度后期导致不自然

## P-003 极简画框留白
tags: [排版, 品牌, 画册]
features:
  - 大面积白底（>60% 留白）
  - 细体无衬线英文标题
  - 产品或人物居中
  - 宽字距
  - 信息极度克制
use_when: Brand Deck、Lookbook 封面、Banner、详情页分隔
fragments: [F-003]
prompt_template: |
  minimalist layout, large white space, centered product,
  thin sans-serif English text, wide letter spacing,
  Lemaire lookbook aesthetic
avoid:
  - 中文用圆体（应该用细黑体）
  - 信息堆砌
  - 装饰性元素过多
