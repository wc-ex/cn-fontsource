### 适用于浏览器加载的免费字体集

- 资源来源于互联网，仅包含免费可商用字体集
- 浏览器使用个性化中文字体较为麻烦，巨大的字体库使得网站加载速度无法忍受，虽然有些网站提供了在线转换的 API，但无法独立部署和兼容性性能等都存在问题。
- 本项目期望尽可能提升中文字库加载速度，以达成中文字库的可用性

### 技术和方案

- 本项目将汉字根据常用情况分为 L1, L2, L3 三级,参考: L1.txt L2.txt 文件
- 通过分离字库方式实现汉字的分段按需加载
- L1 级汉字被分割为 256 个汉字一个文件, 大约 1000 个常用汉字左右
- L2 级汉字被分割为 128 个汉字一个文件, 大约 2500 个常用字
- L3 级汉字为字库中的其他部分，按照 32 个汉字一个文件进行分割，以提升非常用汉字的加载速度。
- 将字库转换为 woff2 格式，进行字库压缩

### 优化

> 本项目目前使用的 L1,L2 汉字列表尚有优化空间，目前列表是从互联网搜索摘录，感觉和当前网络中汉字使用频率并非完全吻合。
> 理想做法应通过爬虫爬取常用网站，统计出当前使用频率最高的汉字集合，取前 3000-4000 个。有条件的朋友可以尝试帮助我们完善这个列表。

### 使用

- 可通过 npm 本地安装字体包
- 也可直接使用 jsdelivr 直接 CDN 加载, 参见具体字体包

### 推荐收录新字体

- 字体必须为免费商用版本
- 查找是否已经存在相同字体
- 提交 ISSUES, 参考 fonts 目录下文件格式提交描述 JSON
- 确保 download 字段可用, 如某些网站无固定下载路径，可先下载后上传到 github 自己账户的项目中
- 下载路径的源字体为 TTF 或者 OTF 格式
- 下载路径可以是压缩包，请检查压缩包内的路径，并正确填写 fontFile 字段
- 查看来源字体压缩包，如有版权相关附加文件信息，请正确添加到 extraFiles 字段
- 确保 link 字段为有效来源 URL

#### 样例

```json
{
  "name": "字体圈欣意吉祥宋",
  "description": "字体圈欣意吉祥宋",
  "version": "1.0.26",
  "fontFile": "ZiTiQuanXinYiJiXiangSong/ZiTiQuanXinYiJiXiangSong-2.ttf",
  "extraFiles": [
    "ZiTiQuanXinYiJiXiangSong/字体圈欣意吉祥宋授权证书.jpg",
    "ZiTiQuanXinYiJiXiangSong/《吉祥宋》字体必读声明及使用范畴.txt"
  ],
  "download": "https://download.fastgit.org/wc-one/cn-font/releases/download/init/ZiTiQuanXinYiJiXiangSong.zip",
  "link": "https://www.fonts.net.cn/font-39072283843.html",
  "license": "free"
}
```

##### 觉得有用请随手加星

### 字体列表

- _思源宋体-中日韩简繁_ (44748 字): [字体包](https://www.npmjs.com/package/@wc1font/source-han-serif-sc-vf) [来源网站](https://github.com/adobe-fonts/source-han-serif)
- _思源宋体-简_ (30897 字): [字体包](https://www.npmjs.com/package/@wc1font/source-han-serif-cn-vf) [来源网站](https://github.com/adobe-fonts/source-han-serif)
- _思源黑体-简_ (30897 字): [字体包](https://www.npmjs.com/package/@wc1font/source-han-serif-cn-vf) [来源网站](https://github.com/adobe-fonts/source-han-serif)
- _思源黑体-中日韩简繁_ (30897 字): [字体包](https://www.npmjs.com/package/@wc1font/source-han-serif-cn-vf) [来源网站](https://github.com/adobe-fonts/source-han-sans)
- _字体圈欣意吉祥宋_ (7238 字): [字体包](https://www.npmjs.com/package/@wc1font/fontquan-xin-yi-ji-xiang-song) [来源网站](https://www.fonts.net.cn/font-39072283843.html)
- _鸿雷板书简体_ (6996 字): [字体包](https://www.npmjs.com/package/@wc1font/honglei-sim) [来源网站](https://www.fonts.net.cn/font-38386302876.html)

- _演示秋鸿楷_ (6971字): [字体包](https://www.npmjs.com/package/@wc1font/slideqiuhong) [来源网站](https://www.fonts.net.cn/font-38836352052.html)
- _方正楷体简体_ (8098字): [字体包](https://www.npmjs.com/package/@wc1font/fz-kai-z-03-s) [来源网站](https://www.fonts.net.cn/font-31561199974.html)