# JetBrains 配色色号手册

> **数据来源（2026-11-04 采集）**
> - **图标渐变版**：本机安装的 JetBrains 2026.x IDE 目录下 `bin/*.svg`（IntelliJ IDEA、PyCharm、WebStorm、GoLand、Rider、DataGrip、DataSpell、RustRover）
> - **其他产品 Logo**：JetBrains 官方品牌资源 `resources.jetbrains.com/storage/products/company/brand/logos/*.svg`
> - **网页配色**：jetbrains.com 线上样式表（设计系统 CSS 变量）
> - **GoLand 页面 CSS**：`https://www.jetbrains.com/go/` 引用的 31 个样式表，详见第 7 节
> - 所有色值为 **sRGB HEX**；`#RRGGBBAA` 的第 7–8 位是透明度（00 = 全透明，FF = 不透明）
> - 渐变节点写作「位置 → 颜色」，位置是 SVG `offset` 百分比

---

## 0. 速查：最常用的 12 个颜色

| 用途 | 色号 |
|---|---|
| JetBrains 品牌渐变（起 / 中 / 止） | `#FF9419` → `#FF021D` → `#E600FF` |
| 官网主色（浅色主题） | `#6B57FF` |
| 官网主色（深色主题） | `#8473FF` |
| 官网深色底 / 主文字 | `#19191C` |
| 官网纯白 / 深色模式文字 | `#FFFFFF` |
| 图标底板黑 | `#000000` |
| 产品图标主蓝 | `#007DFE` |
| 产品图标主青 | `#01C4F4` |
| 产品图标主绿 | `#00D886` |
| 产品图标主黄 | `#F0EB19` |
| 产品图标主粉红 | `#FE2857` |
| 产品图标主紫 | `#7256FF` |

---

## 1. 公司标识：JetBrains Logo

官方 `jetbrains.svg`（含图形标 + 文字标）。

| 部位 | 色号 | 说明 |
|---|---|---|
| 图形标渐变 · 起点 | `#FF9419` | 橙色，位于图形左下 |
| 图形标渐变 · 43% | `#FF021D` | 正红，渐变主体 |
| 图形标渐变 · 99% | `#E600FF` | 品红，位于图形右上 |
| 图形标内部方框 | `#000000` | 纯黑方块 |
| 图形标内部笔画 | `#FFFFFF` | 纯白 |
| 文字标 "JetBrains" | `#000000` | 黑色字（深色底需换白字） |

> 渐变类型：线性渐变，方向为左下 → 右上。

---

## 2. 产品图标（安装包 / 官方品牌 SVG 的渐变版）

每个图标由 **3 个彩色几何块 + 1 个黑色底板 + 白色字形** 构成：
- 渐变 A、渐变 B 是 SVG 中两条 `linearGradient`
- 「纯色块」是第三个不带渐变的彩色块
- 底板固定 `#000000`，字形固定 `#FFFFFF`（下表不再重复）

### 2.1 IDE 系列

| 产品 | 渐变 A | 渐变 B | 纯色块 |
|---|---|---|---|
| **IntelliJ IDEA** | 10% `#FC801D` → 59% `#FE2857` | 21% `#FE2857` → 70% `#007EFF` | `#FF8100` |
| **PyCharm** | 10% `#00D886` → 59% `#F0EB18` | 30% `#F0EB18` → 70% `#00C4F4` | `#00D886` |
| **WebStorm** | 22% `#F0EB18` → 59% `#00C4F4` | 19% `#00C4F4` → 83% `#007DFE` | `#F0EB18` |
| **GoLand** | 24% `#00D886` → 51% `#007DFE` | 27% `#007DFE` → 70% `#D249FC` | `#00D886` |
| **PhpStorm** | 16% `#D249FC` → 55% `#FF2D90` | 30% `#FF2D90` → 70% `#7256FF` | `#D249FC` |
| **CLion** | 29% `#009AE5` → 70% `#00D980` | 30% `#FF318C` → 54% `#009AE5` | `#FF318C` |
| **RubyMine** | 29% `#FF2358` → 75% `#7256FF` | 29% `#FF8100` → 56% `#FF2358` | `#FF8100` |
| **Rider** | 21% `#007DFE` → 55% `#FFB700` | 23% `#FFB700` → 73% `#FF0A67` | `#007DFE` |
| **DataGrip** | 28% `#7256FF` → 66% `#00D980` | 30% `#FF43F2` → 54% `#7256FF` | `#FF43F2` |
| **DataSpell** | 28% `#007DFE` → 73% `#00D980` | 32% `#F0EB18` → 55% `#007DFE` | `#F0EB18` |
| **RustRover** | 8% `#00D886` → 46% `#FFAB00` | 19% `#FFAB00` → 83% `#FF004C` | `#00D886` |

### 2.2 .NET 工具链

| 产品 | 渐变 A | 渐变 B | 纯色块 |
|---|---|---|---|
| **ReSharper** | 29% `#FF45ED` → 70% `#FF0A67` | 30% `#FDB60D` → 54% `#FF45ED` | `#FDB60D` |
| **ReSharper C++** | 无渐变（网页版单色） | — | `#FF45ED` |
| **dotTrace** | 18% `#6B57FF` → 54% `#FF2358` | 12% `#FF2358` → 92% `#FF45ED` | `#6B57FF` |
| **dotMemory** | 31% `#FF45ED` → 83% `#6B57FF` | 30% `#FDB60D` → 70% `#FF45ED` | `#FDB60D` |
| **dotCover** | 18% `#6B57FF` → 54% `#FF45ED` | 12% `#FF45ED` → 92% `#FC801D` | `#6B57FF` |
| **dotPeek** | 29% `#6B57FF` → 89% `#07C3F2` | 30% `#FF45ED` → 84% `#6B57FF` | `#FF45ED` |

### 2.3 团队协作与平台

| 产品 | 渐变 A | 渐变 B | 纯色块 |
|---|---|---|---|
| **TeamCity** | 10% `#3BEA62` → 59% `#6B57FF` | 26% `#6B57FF` → 65% `#07C3F2` | `#3BEA62` |
| **YouTrack** | 0% `#FB43FF` → 97% `#FB406D` | 仅一条渐变 | 无 |
| **Hub** | 25% `#7256FF` → 73% `#00C4F4` | 30% `#F0EB18` → 58% `#7256FF` | `#F0EB18` |
| **Qodana** | 10% `#7256FF` → 59% `#FF2D90` | 21% `#FF2D90` → 70% `#FF8200` | `#7256FF` |
| **Datalore** | 10% `#3BEA62` → 59% `#F0EB18` | 26% `#F0EB18` → 65% `#087CFA` | `#3BEA62` |
| **Toolbox App** | 4% `#FC801D` → 38% `#FE2857` → 99% `#AF1DF5` | 仅一条三色渐变 | 无 |

### 2.4 语言、AI 与其他

| 产品 | 色值 | 说明 |
|---|---|---|
| **Kotlin** | 径向 `#E44857` (0%) → `#C711E1` (50.4%) → `#7F52FF` (100%) | 品牌主色 `#7F52FF`，紫红渐变 |
| **Junie**（AI 助手） | `#48E054` | 单一亮绿，无渐变 |
| **All Products Pack** | `#FC801D` + `#F001A0` | 橙 + 洋红两块 |
| **JetBrains Academy** | `#000000` / `#FFFFFF` | 纯黑白 |
| **Space**（已停用） | ① 0% `#FCF84A` → 32% `#AAE681` → 79% `#35CDD1` → 100% `#07C3F2`<br>② 0% `#3BEA62` → 100% `#087CFA`<br>③ 0% `#009AE5` → 18% `#048FDC` → 49% `#1073C5` → 89% `#2346A1` → 100% `#293896` | 三条渐变，仅供历史参考 |

---

## 3. 产品图标（jetbrains.com 产品页的扁平版）

官网产品卡片用的是**无渐变扁平色块**，与安装包里的渐变版存在细微差异（例如 IDEA 官网用 `#017EFE`，安装包渐变用 `#007EFF`）。

| 产品 | 色块 A | 色块 B | 色块 C |
|---|---|---|---|
| IntelliJ IDEA | `#017EFE` | `#FE2857` | `#FF8100` |
| PyCharm | `#00D886` | `#F0EB19` | `#01C4F4` |
| WebStorm | `#01C4F4` | `#007DFE` | `#F0EB19` |
| PhpStorm | `#FF2D90` | `#D249FC` | `#7357FF` |
| GoLand | `#00D886` | `#D249FC` | `#007DFE` |
| Rider | `#007DFE` | `#FEB601` | `#FE2857` |
| CLion | `#FF318C` | `#009AE5` | `#00D886` |
| RubyMine | `#7256FF` | `#FE2857` | `#FF8100` |
| DataGrip | `#FF43F2` | `#7155FE` | `#00D886` |
| RustRover | `#00D886` | `#FEAB01` | `#FF004C` |
| ReSharper | `#FDB60D` | — | — |
| ReSharper C++ / dotPeek | `#FF45ED` | — | — |
| dotTrace / dotCover | `#6B57FF` | — | — |
| dotMemory | `#FDB60D` | — | — |
| TeamCity | `#3BEA62` | — | — |
| Datalore | `#3BEA62` | — | — |
| Hub | `#F0EB18` | — | — |
| Qodana | `#7256FF` | — | — |
| All Products Pack | `#FC801D` | `#F001A0` | — |
| YouTrack | `#FB43FF` → `#FB406D` | 渐变 | — |
| JetBrains Academy | `#000000` | `#FFFFFF` | — |

---

## 4. 官网 / 网页设计配色（jetbrains.com 设计系统）

### 4.1 基础中性色

| 名称 | 色号 | 典型用途 |
|---|---|---|
| Black | `#19191C` | 全站深色底、正文主色（不是纯黑） |
| White | `#FFFFFF` | 浅色底、深色模式文字 |
| Grey 5 | `#F4F4F4` | 浅灰背景 |
| Grey 10 | `#E8E8E8` | 分隔线、浅色块 |
| Grey 20 | `#D1D1D2` | 边框 |
| Grey 30 | `#BABABB` | 禁用态文字 |
| Grey 40 | `#A3A3A4` | 占位符 |
| Grey 50 | `#8C8C8E` | 次级文字 |
| Grey 60 | `#757577` | 次级文字（深） |
| Grey 70 | `#5E5E60` | 正文辅助 |
| Grey 80 | `#474749` | 深色模式边框 |
| Grey 90 | `#303033` | 深色模式卡片 |
| Grey 95 | `#252528` | 深色模式面板 |
| Legacy Dark | `#27282C` | 旧版站点正文色 |
| Hero Black | `#000000` | 首页主视觉纯黑底 |
| Deep Panel | `#14141E` | 深色渐变端色 |

### 4.2 黑色透明度阶梯（`#19191C` + 透明度）

| 等级 | 色号 | 不透明度 |
|---|---|---|
| black-t5 | `#19191C0D` | 5% |
| black-t10 | `#19191C1A` | 10% |
| black-t20 | `#19191C33` | 20% |
| black-t30 | `#19191C4D` | 30% |
| black-t40 | `#19191C66` | 40% |
| black-t50 | `#19191C80` | 50% |
| black-t60 | `#19191C99` | 60% |
| black-t70 | `#19191CB3` | 70% |
| black-t80 | `#19191CCC` | 80% |
| black-t90 | `#19191CE6` | 90% |
| black-t95 | `#19191CF2` | 95% |

### 4.3 白色透明度阶梯（`#FFFFFF` + 透明度）

| 等级 | 色号 | 不透明度 |
|---|---|---|
| white-t5 | `#FFFFFF0D` | 5% |
| white-t10 | `#FFFFFF1A` | 10% |
| white-t20 | `#FFFFFF33` | 20% |
| white-t30 | `#FFFFFF4D` | 30% |
| white-t40 | `#FFFFFF66` | 40% |
| white-t50 | `#FFFFFF80` | 50% |
| white-t60 | `#FFFFFF99` | 60% |
| white-t70 | `#FFFFFFB3` | 70% |
| white-t80 | `#FFFFFFCC` | 80% |
| white-t90 | `#FFFFFFE6` | 90% |
| white-t95 | `#FFFFFFF2` | 95% |

### 4.4 主色（Primary）五档

| 档位 | 浅色主题 | 深色主题 | 含义 |
|---|---|---|---|
| primary | `#6B57FF` | `#8473FF` | 主按钮、链接、强调 |
| primary-dim | `#8979FF` | `#6F61D2` | 次级强调、hover 备选 |
| primary-fog | `#E1DDFF` | `#2E2B49` | 淡色背景块 |
| primary-t-dim | `#6B57FFCC` | `#8473FFCC` | 主色 80% 透明 |
| primary-t-fog | `#6B57FF33` | `#8473FF4D` | 主色 20% / 30% 透明（浅底/深底） |

> 注：官网根变量中深色主题主色为 `#8473FF`；但 `page-color-default-purple` 页面主题块把深浅两套都设为 `#6B57FF`。做还原时按具体页面取值。

### 4.5 语义色

| 语义 | 浅色主题 | 深色主题 | 背景色（20% 透明） |
|---|---|---|---|
| Success 成功 | `#4DBB5F` | `#4DBB5F` | `#4DBB5F33` |
| Warning 警告 | `#F3C033` | `#F3C033` | `#F3C03333` |
| Danger 危险 | `#CC1400` | `#FF6553` | 浅 `#CC140033` / 深 `#FF655333` |

### 4.6 官网命名主题色板（`page-color-*`）

官网每套主题包含「主色 + 浅色 dim + 浅色 fog + 深色 dim + 深色 fog」五个值，共 11 套。

| 主题名 | 主色 | dim（浅色） | fog（浅色） | dim（深色） | fog（深色） |
|---|---|---|---|---|---|
| default-purple | `#6B57FF` | `#8979FF` | `#E1DDFF` | `#5646CC` | `#151133` |
| deep-blue | `#0047FD` | `#336CFD` | `#CCDAFF` | `#0039CA` | `#000E33` |
| lake-blue | `#0068FD` | `#3386FD` | `#CCE1FF` | `#0053CA` | `#001533` |
| sky-blue | `#007BFF` | `#3395FF` | `#CCE5FF` | `#0062CC` | `#001933` |
| amethyst-purple | `#7E42FF` | `#9868FF` | `#E5D9FF` | `#6535CC` | `#190D33` |
| lilac-purple | `#671FFF` | `#854CFF` | `#E1D2FF` | `#5219CC` | `#150633` |
| orchid-purple | `#8D48FF` | `#A46DFF` | `#E8DAFF` | `#713ACC` | `#1C0E33` |
| ocean-green | `#088484` | `#399D9D` | `#CEE6E6` | `#066A6A` | `#021A1A` |
| forest-green | `#00874D` | `#339F71` | `#CCE7DB` | `#006C3E` | `#001B0F` |
| berry-pink | `#DF2477` | `#E55092` | `#F9D3E4` | `#B21D5F` | `#2D0718` |
| fuchsia-pink | `#E20F86` | `#E83F9E` | `#F9CFE7` | `#B50C6B` | `#2D031B` |

> 每套还有对应 80% / 20% 透明版：`主色 + CC`、`主色 + 33`。

### 4.7 其他网页用色

| 用途 | 色号 | 说明 |
|---|---|---|
| 链接 / 购物车角标 | `#167DFF` | 旧版站点主蓝 |
| 深色模式链接 | `#4CA6FF` | 深色底上的链接蓝 |
| 滚动条滑块 | `#7B61FF` | 首页长列表自定义滚动条 |
| 标签渐变 | `#5A1FD0` → 透明 | 131° 线性渐变 |
| 首页强调粉 | `#F31199` | 主视觉数字/装饰 |
| Datalore 渐变端点 | `#087CFA` | 青 → 蓝 |
| 辅助蓝 | `#009AE5` | 图标与插画 |
| 辅助青 | `#07C3F2` | 图标与插画 |

---

## 5. 近似色辨析（最容易拿错的一组）

### 蓝色系

| 色号 | 出处 |
|---|---|
| `#017EFE` | IntelliJ IDEA 官网扁平图标 |
| `#007EFF` | IntelliJ IDEA 安装包渐变端点 |
| `#007DFE` | WebStorm / GoLand / Rider / DataSpell 图标主蓝 |
| `#007BFF` | 官网 sky-blue 主题 |
| `#167DFF` | 官网旧版链接蓝 |
| `#4CA6FF` | 深色模式链接蓝 |
| `#087CFA` | Datalore 渐变端点 |
| `#009AE5` | CLion 图标渐变端点 |
| `#01C4F4` | 官网扁平图标青 |
| `#00C4F4` | 安装包渐变青 |

### 绿色系

| 色号 | 出处 |
|---|---|
| `#00D886` | PyCharm / GoLand / RustRover 主绿 |
| `#00D980` | CLion / DataGrip / DataSpell 渐变绿 |
| `#3BEA62` | TeamCity / Datalore 亮绿 |
| `#48E054` | Junie 绿 |
| `#4DBB5F` | 官网 Success |
| `#00874D` | 官网 forest-green |
| `#088484` | 官网 ocean-green |

### 黄色 / 橙色系

| 色号 | 出处 |
|---|---|
| `#F0EB19` | PyCharm / WebStorm 图标黄 |
| `#F0EB18` | 官网扁平图标黄 |
| `#FDB60D` | ReSharper / dotMemory |
| `#FEB601` | Rider 官网扁平图标黄 |
| `#FFAB00` | RustRover 渐变黄 |
| `#FFB700` | Rider 渐变黄 |
| `#FF8100` | IntelliJ IDEA 纯色块 |
| `#FEAB01` | RustRover 官网扁平图标黄 |
| `#FC801D` | Toolbox / All Products Pack 橙 |
| `#FF8200` | Qodana 渐变橙 |
| `#FF9419` | JetBrains 公司标识渐变起点 |

### 红色 / 粉色 / 洋红系

| 色号 | 出处 |
|---|---|
| `#FE2857` | IntelliJ IDEA / Rider 粉红 |
| `#FF2358` | RubyMine / dotTrace |
| `#FF318C` | CLion 粉 |
| `#FF2D90` | PhpStorm 粉 |
| `#FF0A67` | ReSharper 玫红 |
| `#FF004C` | RustRover 端点红 |
| `#FF45ED` | ReSharper C++ / dotPeek 洋红 |
| `#FB43FF` | YouTrack 渐变起点 |
| `#FB406D` | YouTrack 渐变终点 |
| `#DF2477` | 官网 berry-pink |
| `#E20F86` | 官网 fuchsia-pink |
| `#F31199` | 首页强调粉 |
| `#CC1400` | 官网 Danger（浅色） |
| `#FF6553` | 官网 Danger（深色） |
| `#F001A0` | All Products Pack 洋红 |
| `#E44857` | Kotlin 渐变外圈 |
| `#C711E1` | Kotlin 渐变中段 |

### 紫色系

| 色号 | 出处 |
|---|---|
| `#6B57FF` | JetBrains 官网主紫 |
| `#8473FF` | 官网主紫（深色主题） |
| `#7256FF` | PhpStorm / DataGrip / RubyMine / Qodana / Hub |
| `#7155FE` | DataGrip 官网扁平图标紫 |
| `#7357FF` | PhpStorm 官网扁平图标紫 |
| `#7F52FF` | Kotlin 品牌主紫 |
| `#7E42FF` | 官网 amethyst-purple |
| `#8D48FF` | 官网 orchid-purple |
| `#671FFF` | 官网 lilac-purple |
| `#AF1DF5` | Toolbox 渐变终点 |
| `#5A1FD0` | 首页标签渐变 |
| `#7B61FF` | 官网滚动条 |

---

## 6. 还原 / 使用建议

1. **画产品图标**：用 64×64 画布，先铺黑色 `#000000` 底板，再叠 3 个彩色块（两渐变 + 一纯色），最后放白色 `#FFFFFF` 字形。渐变版优先级高于官网扁平版，因为它是安装包里实际显示的版本。
2. **深色页面**：底色用 `#19191C`（不要用纯黑），主文字 `#FFFFFF`，次级文字 `#FFFFFF99`（60%），最弱文字 `#FFFFFF4D`（30%）。
3. **浅色页面**：底色 `#FFFFFF`，正文 `#19191C`，次级 `#19191C99`，边框 `#19191C1A`。
4. **主按钮**：浅色主题 `#6B57FF` + 白字；hover 用 `#8979FF`；按下可用 dim 深色 `#5646CC`。深色主题主色换 `#8473FF`。
5. **浅色强调块**：用 fog 色 `#E1DDFF`，配 `#6B57FF` 文字，对比度足够且不刺眼。
6. **语义提示**：成功 `#4DBB5F`、警告 `#F3C033`、危险 `#CC1400`；背景统一取同色 + `33`（20% 透明）。
7. **品牌物料**：JetBrains 公司标识必须用 `#FF9419 → #FF021D → #E600FF` 渐变，不要用官网主紫替代。
8. **颜色数量说明**：同一产品在「官网扁平图标」和「安装包渐变图标」中的色号并不完全一致（如 `#017EFE` vs `#007EFF`），本文两套都保留，按使用场景取用。

---

## 7. GoLand 官网 CSS 采集与设计语言（2026-11-04）

> 采集对象：`https://www.jetbrains.com/go/` 页面引用的 31 个线上样式表（约 753 KB）。
> 目的：提取官网真实使用的表面色、阴影、圆角、字体、动效参数，作为本项目深色 GoLand 主题的设计依据。

### 7.1 表面与中性色（官网实际变量）

| CSS 变量 | 色号 | 用途 |
|---|---|---|
| `--rs-color-black` | `#19191C` | 全站深色底、正文主色 |
| `--rs-color-white` | `#FFFFFF` | 浅色底、深色模式文字 |
| `--rs-color-grey-5` | `#F4F4F4` | 浅灰背景 |
| `--rs-color-grey-10` | `#E8E8E8` | 分隔线 |
| `--rs-color-grey-20` | `#D1D1D2` | 边框 |
| `--rs-color-grey-50` | `#8C8C8E` | 次级文字 |
| `--rs-color-grey-80` | `#474749` | 深色模式强边框 |
| `--rs-color-grey-90` | `#303033` | 深色模式卡片 / 浮层 |
| `--rs-color-grey-95` | `#252528` | 深色模式面板 |
| `#14141E` | 深色渐变端色 | 页面底部压暗 |

透明阶梯：`#19191C0D`（5%）→ `#19191C1A`（10%）→ `#19191C33`（20%）→ `#19191C80`（50%）→ `#19191CF2`（95%）；白色同理 `#FFFFFF0D / 1A / 33 / 4D / 80 / B3 / CC / F2`。

### 7.2 主色与语义色

| 语义 | 浅色 | 深色 |
|---|---|---|
| Primary | `#6B57FF` | `#8473FF` |
| Primary dim | `#8979FF` | `#6F61D2` |
| Primary fog | `#E1DDFF` | `#2E2B49` |
| Primary 80% | `#6B57FFCC` | `#8473FFCC` |
| Primary 20% / 30% | `#6B57FF33` | `#8473FF4D` |
| Link | `#167DFF` | `#4CA6FF` |
| Danger | `#CC1400` | `#FF6553` |
| Success | `#4DBB5F` | `#4DBB5F` |
| Warning | `#F3C033` | `#F3C033` |
| GoLand 品牌绿 / 蓝 / 紫 | `#00D886` / `#007DFE` / `#D249FC` | 同左 |

> 官网设计系统的主交互色是 JetBrains 紫，但 GoLand 产品页的识别色仍是产品 Logo 的绿 / 蓝 / 紫。项目采用「GoLand 品牌三色做功能色 + 官网表面与动效规范」的组合。

### 7.3 字体

| 角色 | 官网字体栈 |
|---|---|
| 标题 / UI | `"JetBrains Sans", Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif` |
| 正文（中文页面） | `"PingFang SC", "HarmonyOS_Medium", "Helvetica Neue", "Microsoft YaHei", sans-serif` |
| 等宽 | `"JetBrains Mono", SFMono-Regular, Consolas, "Liberation Mono", Menlo, Courier, monospace` |
| 装饰数字 | `RankingNumberFont`（榜单数字专用） |

字号：桌面 h1 35px、h2/h3 28px、subtitle 23px；正文 16px、辅助 14/13/12px；首页大数字可达 69–142px。字距以 `.0045em` 为基准，大标题收紧。

### 7.4 圆角 / 阴影 / 描边

| 项目 | 官网实测值 |
|---|---|
| 常用圆角 | `8px`（26 处，最常用）、`4px`（17 处）、`16px`、`24px` |
| 卡片圆角变量 | `--_rs-card-border-radius: 8px / 16px / 24px` |
| 常规阴影 | `0 4px 30px #0000001a` |
| 悬浮阴影 | `0 4px 24px #0003` |
| 描边 | `inset 0 0 0 1px` 细内描边，颜色取 white/black 透明阶梯 |
| 焦点环 | `0 0 0 4px` + `--_rs-color-primary-t-dim`（浅色 `#6B57FFCC`，深色 `#8473FFCC`） |
| 输入框焦点 | 2px 主色内阴影 + 4px 半透明外环 |

### 7.5 动效

| 项目 | 官网实测值 |
|---|---|
| 主过渡 | `transition: background-color .2s ease-in-out`（11 处） |
| 显隐过渡 | `opacity .2s ease` / `opacity .3s` |
| 变换过渡 | `transform .2s / .3s`，缓动 `ease` 或 `--rs-transition-function` |
| 入场动画 | `fadeInTopToBottom / BottomToTop / LeftToRight / RightToLeft`，`0.2s`，位移 `10px` + 透明度 0→1 |
| 图片交互 | hover 时 `transform: scale(1.1)` |
| 数值/图标 | `rs-icon-rotate` 等旋转关键帧；骨架屏、loading 旋转 |

### 7.6 组件模式

1. **卡片**：深色底上使用 `#FFFFFF1A` 半透明表面；浅色底使用纯白；圆角 8px、内容内边距 32px。
2. **按钮**：纯色主按钮 + 白字，focus-visible 时叠加 4px 主色透明环；按下不做位移，靠颜色变化反馈。
3. **主题切换**：官网用 `--_rs-theme-light-coefficient` / `--_rs-theme-dark-coefficient` 两个系数在同一套变量里插值，而不是复制两份样式。
4. **渐变**：官网本身很克制，只有 IDE 截图 `linear-gradient(135deg, #2B2B2B, #3C3F41)`、链接下划线、进度条等少量渐变；品牌 Logo 为扁平三色块。GoLand 主题的渐变色应来自产品 Logo（绿→蓝→紫），而不是官网主紫。

### 7.7 落到本项目的规则

- **表面**：深色继续用 `#19191C` 页面底、`#252528` 卡片、`#303033` 浮层/次级块，新增 `inset 0 1rpx 0 #FFFFFF0F` 顶部高光。
- **阴影**：统一为「1px 内高光 + 8rpx 近距阴影 + 60rpx 大扩散阴影」，深色额外叠一层紫色/蓝色低透明度光晕（`rgba(132,115,255,…)`），对应官网 `0 4px 30px #0000001a`；绿色不再参与大面积光晕。
- **圆角**：沿用 8px 的倍数（16/24/32rpx），封面保留更大的 32rpx 圆角。
- **动效**：入场 0.2–0.56s，位移 10–28rpx，透明度 0→1；交互反馈 0.18–0.2s `ease-in-out`；卡片、列表、统计块、封面、弹层、模块卡全部带阴影和入场/按压动画。
- **字体**：正文与标题回退到系统 UI 无衬线字体栈（`-apple-system / PingFang SC / Microsoft YaHei`），仅封面编号、日期等数字保留 `--mono` 等宽字体；此前的艺术字体试验已撤销。
- **渐变原则**：所有「有颜色的块」都使用 135° 对角渐变，不再出现大面积纯色填充；浅色用同色系浅渐变，深色用低透明度渐变做玻璃感。

### 7.8 本项目深色最终取值（替代早先的绿色方案）

| 角色 | 取值 | 说明 |
|---|---|---|
| 页面底 | `#19191C → #1B1B22 → #211D33 → #14141E` | 近黑中性底，仅尾部带一点冷紫 |
| 卡片 | `#252528 → #262433 → #1F2433` | JetBrains 中性面，轻微偏紫 |
| 次级/浮层 | `#303033` | 输入框、分段条、轨道 |
| 主色 | `#8473FF`（按下 `#6F61D2`） | 官网紫，替代原绿色 |
| 链接/辅色 | `#4CA6FF` | JetBrains 链接蓝 |
| 饮食 | `#007DFE → #4CA6FF` | 蓝 |
| 睡眠 | `#8473FF → #D249FC` | 紫 → 洋红 |
| 日程 | `#01C4F4 → #4CA6FF` | 青 → 蓝 |
| 运动 | `#D249FC → #FF6553` | 洋红 → 橙红 |
| 热度 | `#2A2733 → #342B52 → #4A3B8F → #8473FF` | 紫色梯度，替代绿色热力 |
| 绿色 | `#00D886` | 仅保留在封面渐变最左端的一小段品牌点缀，占比 <15% |
| 阴影光晕 | `rgba(132,115,255,0.14–0.40)` + `rgba(210,73,252,0.30)` | 紫/洋红，替代绿色光晕 |
