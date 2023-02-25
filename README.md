## 适用于浏览器加载的汉字字体集

- 浏览器使用个性化中文字体较为麻烦，巨大的字体库使得网站加载速度无法忍受，虽然有些网站提供了在线转换的 API，但无法独立部署和兼容性性能等都存在问题。
- 本项目通过分段字库方式实现汉字字库的按需加载，期望尽可能提升中文字库加载速度，以达成中文字库在 WEB 端的可用性。
- 我们为分段 WEB 字体直接生成了 css 文件，可通过 CDN 直接引用或者下载包到自己的项目中，详情请参阅每个字体包的说明。
- 本项目仅搜录使用 WEB 中文字体工具制作的可用于 WEB 直接显示的字体集，所有内容内容由网友自行制作并发布到 NPM 仓库。

### ！！非常感谢提供免费和开源的字体作者，让我们能够轻松无忧的使用和体会汉字之美。

### ！！感谢所有字体的作者，让我们看到更精彩多样的汉字。

### ！！也支持商业化字体，付出有了回报，才能有更多优秀作品。

## 欢迎提交新字体，字体制作方法见下面章节。

## 技术方案和更新

本仓库由原有的仓库 https://github.com/wc-one/cn-font/ 仓库迁移而来，更新以下内容：

- 升级和完善了字体制作工具，开放给大家自行使用
- 升级了 L1 和 L2 字库，使用国家字库分级标准。
- L1 级更改为 192 字分包,L2 级更改为 96 字分包,L3 级改为 64 字分包,平衡生成 CSS 和字体实际文件大小。
- L1 和 L2 支持繁体
- 优化了生成的 css 的大小
- 支持本地字库优先引入
- 字体发布到 NPM 的包名，从原有 NPM 组织二级名称，调整到以**cn-fontsource-**为前缀的全名，便于大家自行发布和自动化收录

## 使用

- 可通过 npm 本地安装字体包
- 也可直接使用 jsdelivr 直接 CDN 加载, 在下方页面点击相关字体，可查看字体包相关说明。

## 字体制作和发布

### 安装工具软件
请使用 npm 软件包工具，执行以下命令,也可以使用yarn，pnpm等

```shell
npm install --global @wcex/cn-fontsource
```

安装完成即可直接执行命令: **cn-fontsource**

### 创建和发布字体
1. 注册和创建你的 NPM 账号，https://www.npmjs.com/
2. 确保你的 npm 已经登录，使用以下命令验证: _npm login_
3. 创建字体目录
4. 在字体目录下建立 _font.json5_ 文件, 按以下样例填写（以 **悠哉字体** 为例）
> **请认真核对和填写每一项内容，对使用者负责**

```json5
{
  // 字体名称
  name: "悠哉字体",
  // 字体分类，请按照实际填写
  fontClass: ["悠哉", "手写"],
  // 版本，如此前发布需重新发布，需升级此版本号以便发布到NPM
  version: "1.0.3",
  // 描述信息
  description: "本字体是一款基于 Y.OzFont 的手写风格的字体。利用原字体中已有的笔划和部件，通过拼接和调整造出新字 （必要时自己用鼠标写出部件） 。目前已补全原字体中有对应繁体字的简体字、 GB 2312 范围内的所有汉字 （6763 个） 、《通用规范汉字表》范围内的所有汉字 （8105 个） ，BIG5-2003 范围内的所有汉字 （13058 个，包含台湾教育部门规定的 4808 个常用汉字） 。",
  // 扩展名，仅能英文，当npm存在同名包需要覆盖时用
  ext: "",
  // 类型,必须正确填写: free-免费字体, opensource-开源字体, paid-商业字体
  type: "opensource",
  // 字体来源链接，请确认
  link: "https://github.com/lxgw/yozai-font",
  // 字体授权信息，请确认
  license: "free",
}
```
3. 下载字体文件到此目录, 当前支持 ttf 和 otf 格式。
4. 如同一字体有多个字重，请一并下载到此目录,如不同名称或者风格，请新建目录和起名。
5. 准备好目录后，执行: _cn-fontsource [目录名]_, 即可一键提交发布到NPM。
6. 发布完成后，请到 npm 网站确认发布成功。 https://www.npmjs.com/
> 提交新字体后，请在 https://github.com/wc-ex/cn-fontsource/issues 中发布消息提醒我们更新字体目录。
> 发现自动收录字体有版权风险或者其他问题也请在 https://github.com/wc-ex/cn-fontsource/issues 提出。


## 以下字体列表为通过 NPM 进行自动索引，内容均为网友自行提交，请使用者自行鉴别，谨防造成不必要的麻烦。使用商业字体请尊重版权和他人劳动成果。
### 点击字体名称可跳转到字体包首页，内有引用说明

<!--@LIST-->
### 开源字体: 11
<p algin="center">
 <a href="https://www.npmjs.com/package/cn-fontsource-lxgw-wen-kai-screen">cn-fontsource-lxgw-wen-kai-screen</a>
 <img src="https://cdn.jsdelivr.net/npm/cn-fontsource-lxgw-wen-kai-screen@1.0.6/font.png" alt="cn-fontsource-lxgw-wen-kai-screen">
</p>
 <a href="https://www.npmjs.com/package/cn-fontsource-yozai">cn-fontsource-yozai</a>
 <img src="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai@1.0.6/font.png" alt="cn-fontsource-yozai">

<a href="https://www.npmjs.com/package/cn-fontsource-yozai-bold">cn-fontsource-yozai-bold</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-bold@1.0.7/font.png" alt="cn-fontsource-yozai-bold">

<a href="https://www.npmjs.com/package/cn-fontsource-yozai-light">cn-fontsource-yozai-light</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-light@1.0.6/font.png" alt="cn-fontsource-yozai-light">
<a href="https://www.npmjs.com/package/cn-fontsource-yozai-medium">cn-fontsource-yozai-medium</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-medium@1.0.6/font.png" alt="cn-fontsource-yozai-medium">
<a href="https://www.npmjs.com/package/cn-fontsource-yozai-regular">cn-fontsource-yozai-regular</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-regular@1.0.7/font.png" alt="cn-fontsource-yozai-regular">
<a href="https://www.npmjs.com/package/cn-fontsource-yozai-light-regular">cn-fontsource-yozai-light-regular</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-light-regular@1.0.7/font.png" alt="cn-fontsource-yozai-light-regular">
<a href="https://www.npmjs.com/package/cn-fontsource-yozai-medium-regular">cn-fontsource-yozai-medium-regular</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-medium-regular@1.0.7/font.png" alt="cn-fontsource-yozai-medium-regular">
<a href="https://www.npmjs.com/package/cn-fontsource-lxgw-wen-kai-gb-screen">cn-fontsource-lxgw-wen-kai-gb-screen</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-lxgw-wen-kai-gb-screen@1.0.6/font.png" alt="cn-fontsource-lxgw-wen-kai-gb-screen">
<a href="https://www.npmjs.com/package/cn-fontsource-lxgw-wen-kai-screen-r">cn-fontsource-lxgw-wen-kai-screen-r</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-lxgw-wen-kai-screen-r@1.0.6/font.png" alt="cn-fontsource-lxgw-wen-kai-screen-r">
<a href="https://www.npmjs.com/package/cn-fontsource-lxgw-wen-kai-gb-screen-r">cn-fontsource-lxgw-wen-kai-gb-screen-r</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-lxgw-wen-kai-gb-screen-r@1.0.6/font.png" alt="cn-fontsource-lxgw-wen-kai-gb-screen-r">
### 免费字体: 6
<a href="https://www.npmjs.com/package/cn-fontsource-hongleixingshu">cn-fontsource-hongleixingshu</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-hongleixingshu@1.0.6/font.png" alt="cn-fontsource-hongleixingshu">
<a href="https://www.npmjs.com/package/cn-fontsource-slideqiuhong-regular">cn-fontsource-slideqiuhong-regular</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-slideqiuhong-regular@1.0.6/font.png" alt="cn-fontsource-slideqiuhong-regular">
<a href="https://www.npmjs.com/package/cn-fontsource-honglei-sim-regular">cn-fontsource-honglei-sim-regular</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-honglei-sim-regular@1.0.6/font.png" alt="cn-fontsource-honglei-sim-regular">
<a href="https://www.npmjs.com/package/cn-fontsource-hong-lei-zhuo-shu-regular">cn-fontsource-hong-lei-zhuo-shu-regular</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-hong-lei-zhuo-shu-regular@1.0.6/font.png" alt="cn-fontsource-hong-lei-zhuo-shu-regular">
<a href="https://www.npmjs.com/package/cn-fontsource-fz-fang-song-z-02-s-regular">cn-fontsource-fz-fang-song-z-02-s-regular</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-fz-fang-song-z-02-s-regular@1.0.7/font.png" alt="cn-fontsource-fz-fang-song-z-02-s-regular">
<a href="https://www.npmjs.com/package/cn-fontsource-fontquan-xin-yi-ji-xiang-song-regular">cn-fontsource-fontquan-xin-yi-ji-xiang-song-regular</a><img src="https://cdn.jsdelivr.net/npm/cn-fontsource-fontquan-xin-yi-ji-xiang-song-regular@1.0.7/font.png" alt="cn-fontsource-fontquan-xin-yi-ji-xiang-song-regular">
</p>
### 商业字体: 0
<p>
</p>
