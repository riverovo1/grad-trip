# 一起毕业 · 毕业旅行拼团规划

在线作品：https://riverovo1.github.io/grad-trip/

设计说明：https://riverovo1.github.io/grad-trip/research.html

## 产品主线

面向毕业旅行熟人小队，先满足每个人的可用时间与预算，再把偏好转化为可确认的方案，最后衔接行程、预订准备和分账。

- 目的地偏好投票，支持切换演示成员。
- 逐人交通与预算估算，共同时间交集、冲突解释、可采纳的折中建议。
- 共同基础版与体验完整版；自选项目按实际参与人分摊。
- 方案版本确认；日期、预算、成员或行程变化后，旧确认自动失效。
- 邀请快照与成员 JSON 回执，核对后合并，旧方案回执不会被当作当前同意。
- 可编辑 / 导出逐日行程，预订核价清单与平台官网入口。
- AA 账本、精确到分的分摊、结算建议、记录 / 撤销已在其他渠道完成的转账、CSV 导出。
- 首页提供 60 秒体验引导；设计说明呈现公开资料、需求假设、竞品功能对比、设计取舍与验证计划。

## 研究边界

已完成公开资料桌面研究，未开展真实访谈、问卷或真实小队试用。小队与报价均为演示数据，不代表业务成绩。来源与设计推论见 research.html。

## 当前能力边界

GitHub Pages 托管静态页面，数据保存在访问者的浏览器 localStorage。邀请链接携带快照；JSON 回执支持核对合并，暂不支持实时同步或真实身份认证。规则与模板规划未调用在线大模型，价格是可解释的示例估算，没有读取商家实时库存。账本只记录信息，不发起付款。

## 发布与更新

GitHub Pages 从 master 分支仓库根目录发布。无需安装依赖或构建，提交到 master 即触发更新。保持用户名、仓库名与 Pages 配置不变即可保持当前链接。

页面代码、字体回退与图片均不依赖外部 CDN。平台核价入口与研究来源仅在点击时访问。

## 本地预览与测试

在仓库根目录运行 python -m http.server 8000，访问 http://localhost:8000 。

Node.js 18+ 可执行：

    node tests/decision.test.cjs

覆盖约束可行性、无共同日期、预算不足、确认失效、成员视角切换、分摊及结算金额守恒。发布前另使用真实 Chromium 验证桌面、移动端、六成员确认、回执合并与过期处理、CSV 导出、快照导入和研究页。

## 本地图片与授权

- assets/dali.jpg：Mattia Marinolli，CC BY-SA 3.0，https://commons.wikimedia.org/wiki/File:LandscapeDali.jpg
- assets/xiamen.jpg：Jakob Montrasio，CC BY 2.0，https://commons.wikimedia.org/wiki/File:Gulangyu.jpg
- assets/chengdu.jpg：Charlie fong / 冯成，Public domain，https://commons.wikimedia.org/wiki/File:Anshunlang_bridge_Chengdu.jpg

图片使用 Wikimedia 提供的缩略图，未作内容修改；完整署名、来源与许可证链接位于 research.html。

GitHub Pages 的大陆可达性受网络影响，当前环境的访问验证不能代表所有大陆网络。
