FocusFlow Art - Pro 🍅
FocusFlow Art - Pro 是一款将“极致美学”与“工业级并行逻辑”融合的 Web 番茄钟。它不再仅仅是一个简单的计时工具，而是一个基于状态机设计的效率引擎。

🎨 视觉美学与构图 (Aesthetic & Composition)
作为追求审美顶端的作品，本项目在视觉设计上遵循了以下原则：

几何极简主义插画：左上角采用抽象 SVG 番茄构图，打破传统的中心对称，通过“破局”增加页面的动感与灵气。

极致玻璃拟态 (Glassmorphism)：利用 backdrop-filter: blur(40px) 与微弱的内发光边框，营造出悬浮在光晕上的半透明晶体质感。

环境光效 (Ambient Glow)：背景注入动态流动的弥散光斑，随模式切换（专注模式/休息模式）平滑改变色彩频率，引导大脑进入特定的心理状态。

⚙️ 核心技术架构 (Technical Architecture)
1. 并发计时引擎 (Concurrent State Management)
这是本项目最核心的“底层逻辑”。

非阻塞并行机制：传统番茄钟切换视图即暂停，而本项目采用统一的 State Object 驱动。无论你在 UI 上看哪个页面，后台的“专注”与“休息”计时器均独立运行。

全局心跳观察者 (Global Heartbeat)：通过单一的 setInterval 监听器驱动整个系统，确保在多任务并行时依然保持毫秒级的同步精度，且不会造成内存泄漏。

2. 精准位移数字引擎 (Slot-style Transition)
为了彻底解决 Web 渲染中 3D 翻转的不稳定性，本项目开发了“滚轮槽位式”动力系统：

垂直序列渲染：每个数字位预渲染 0-9 垂直列表。

位移变换逻辑：通过 translateY(-digit * 90px) 进行硬编码级别的精准位移。

贝塞尔曲线优化：引入 cubic-bezier(0.4, 0, 0.2, 1.4) 弹性曲线，模拟物理滚轮停顿时产生的轻微回弹。

🛠️ 技术栈 (Tech Stack)
HTML5 / CSS3 (Tailwind CSS)：负责响应式布局与极致的视觉表现。

Vanilla JavaScript (ES6+)：负责核心并发逻辑与 DOM 操作。

JetBrains Mono & Inter Fonts：选用高可读性的开源字体，平衡理性的代码美感与感性的阅读体验。

📦 快速开始 (Quick Start)
该项目为零依赖纯静态页面，克隆即可运行。

克隆仓库

Bash

git clone https://github.com/YourUsername/FocusFlow-Art-Pro.git
运行项目 直接用浏览器打开 index.html 即可体验。

🧠 设计背后的底层逻辑
状态优于展示：在系统设计中，数据（State）永远是第一位的。UI 只是数据的一种表达形式。

认知负荷最小化：通过色彩心理学（红-专注/绿-放松）降低用户的决策成本，帮助用户在 0.8s 内完成心流切换。

CS 肌肉记忆：每一行代码的书写风格都遵循一致性与对称性，不仅为了机器运行，更为了人类阅读。

👤 作者信息
身份：一名 CS 专业大学生，同时也是数学与物理家教。

追求：利用代码重塑世界，热衷于探索社会的底层逻辑。

审美偏好：J Cole (Hip-hop) / 极简主义设计。
