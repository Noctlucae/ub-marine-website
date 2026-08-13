# U B Marine Electrical Sdn. Bhd. — 网站文件说明

## 线上地址
https://voluble-bavarois-d6f34c.netlify.app/
（部署在你自己的Netlify账号nsyit9@gmail.com下，登录 app.netlify.com 可以看到这个站点并管理）

以后每次改完网站，把这个文件夹重新打包/拖到 https://app.netlify.com/drop 上传一次就能更新线上版本（或者登录Netlify后台直接换成绑定Git仓库自动部署，需要的话告诉我）。

**这次更新还没上线**：`网站更新v2.zip` 已经打包好放在这个文件夹里，把它拖到 netlify.com/drop 就能更新成最新版本（Hero背景和About图都换成了真实MSB配电柜照片）。

## 文件
- `index.html` — 单页中英双语网站，打开即用，也可直接部署到任意主机（Vercel / Netlify / 公司自有服务器 / GitHub Pages 皆可）。右上角"中文 / EN"按钮可切换语言。
- `assets/logo.png` — 公司正式logo，已用于导航栏及网站favicon。
- `assets/hero-msb.jpg` — 首页Hero区背景图，真实MSB配电柜阵列照片（原图来自MSB Panel文件夹的efa1810d）。
- `assets/about-msb.jpg` — About Us板块主图，发电机控制盘正面照（原图来自MSB Panel文件夹的291dd810）。
- `assets/gallery-*.jpg` — Our Work板块4张作品展示图（MSB接线、元件装配、舵角指示器、控制台组装）。

## 需要你补充的占位内容（用 Ctrl+F 搜索关键词定位）

| 位置 | 占位内容 | 说明 |
|---|---|---|
| 公司地址 | No. 28, Lorong 4, Jalan Ding Lik Kwong, Sungai Merah, 96000 Sibu, Sarawak | 已根据SSM注册资料更新 |
| 电话 | `+60 16-879 9152（Mr. Yit Nai Soon）`、`+60 16-886 9154（Office）` | 已更新，均已接WhatsApp点击直连（wa.me链接），出现于联系区块+页脚+右下角悬浮按钮 |
| 邮箱可点击 | `mailto:ubest88@hotmail.com` | 联系区块和页脚的邮箱均已改为可点击直接打开邮件客户端 |
| 邮箱 | `ubest88@hotmail.com` | 已更新为实际邮箱，出现2处 |
| 营业时间 | `Mon-Fri 8-5, Sat 8-4.30` | 已更新为实际营业时间 |
| 公司注册号 | `201101002699 (930837-H)` | 已根据SSM注册资料更新，位于页脚 |
| 成立年份/经验年数 | `15+ Years in Operation` | 已根据成立日期25-01-2011计算更新 |
| 完成项目数 | `500+ Projects Completed` | 已更新 |
| 公司/厂房照片 | `assets/about-msb.jpg` + `assets/hero-msb.jpg` | 已替换为真实MSB配电柜实物照（发电机控制盘+大型配电柜阵列），用在About Us主图和Hero背景 |
| 作品展示板块 | `assets/gallery-*.jpg`（4张） | 新增"Our Work / 作品展示"板块，放在服务项目和优势之间，用了盘柜接线、元件装配、舵角指示器、控制台组装4张修图后的照片 |
| Logo | `assets/logo.png` | 已替换为正式logo，用于导航栏和网站favicon |

## 内容框架（基于你的行业背景草拟，可调整）
网站涵盖：公司介绍、六项核心服务（MSB主配电盘制造、船舶电气安装、AutoCAD电路设计、CNC钣金加工、测试调试、维护维修）、四项优势、四步工作流程、联系表单。这些服务项目是根据"主配电盘制造 + 船舶电气 + CNC/AutoCAD"这一行业组合起草的，如与实际业务范围不符，请告诉我需要增删的项目。

## 尚未实现的功能
- 联系表单目前只是弹窗提示，**未连接真实的邮件发送服务**（例如 Formspree、EmailJS 或后端API）。正式上线前需要接入。
- 目前用的是Netlify给的随机域名（voluble-bavarois-d6f34c.netlify.app），如果要换成自己的域名（比如ubmarineelectrical.com），登录Netlify后台可以绑定，或告诉我你买的域名我帮你弄。

## 自查记录
交付前做了一次代码审核，修复了以下问题：
- 移动端（手机/平板宽度）导航栏原本只有CSS样式、没有实际的汉堡菜单按钮和开关逻辑，导致手机用户完全打不开导航菜单——已补上按钮、开关脚本和下拉样式，实测可正常展开收起。
- 中英切换逻辑里，多处区块小标题（如"关于我们""服务项目"等eyebrow标签、地址/电话/邮箱旁的小标签、表单提示文字）在中文模式下会因CSS优先级问题被强制变成行内显示，丢失应有的间距——已统一修正。
- 首页徽章（MARINE & INDUSTRIAL ELECTRICAL SOLUTIONS）在中文模式下也有类似的样式塌陷风险，已加规则修正。
- 切换语言时同步更新了HTML的lang属性（利于屏幕阅读器和搜索引擎正确识别语言）。
- 清理了已不再使用的CSS（占位提示徽章样式）。
- 校验：HTML标签开合配对、CSS大括号配对、所有WhatsApp/邮箱链接格式、JS用到的元素ID全部核对无误。

## 质感优化（参考大型企业官网做的调整）
- logo改用白色圆形底板，避免和藏青色导航栏融为一体；logo放大到64px更醒目。
- 页面滚动时各板块（数据统计、服务卡片、优势卡片、流程步骤等）会依次淡入上滑，不再是一次性生硬出现。
- 顶部导航会自动高亮你正在浏览的板块（About/Services/Why Us/Process/Contact）。
- 点击导航锚点改为平滑滚动，而不是瞬间跳转。
- Hero区背景后来换成了真实MSB配电柜照片（加深色渐变遮罩保证文字清楚），比之前的抽象几何纹理更有说服力。
- 页脚顶部加了一条金色到青色的渐变分隔线，视觉上更精致。
- 这些都是纯样式/交互层面的打磨，没有改动任何文字内容或联系方式。

## 下一步
把以上占位信息发给我，我会直接改好 `index.html`，或者你也可以自己用文本编辑器搜索替换。
