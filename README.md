# 全国各省市烂尾楼停贷通知汇总

## 数据来源统计以及发起人： 已被封禁

*非专业精确数据，仅供参考，与数据模糊分析*

*数据开放转载引用，但请注明出处，非常感谢！*

*这里不做任何非数据性质等其他一系列讨论，只是统计一个数据，有错就纠改，无其他任何含义，别的请勿多言！禁止政治敏感话题！*

*要相信党，相信政府。党和政府一定会给人民群众一个满意的交代，这里仅作数据统计，切勿有过激言论！*

```txt
毛主席在 1962 年七千人大会上的讲话：

https://www.marxists.org/chinese/maozedong/1968/5-016.htm
```

[~~互帮互助留言讨论区=>~~](https://github.com/WeNeedHome/SummaryOfLoanSuspension/discussions)

由于 discussion 的部分聊天不遵守规则，我们关闭了 discussion。

## 相关法律与案例支持

俗话说赤脚的不怕穿鞋的，但是很多中国人是真的只有到了**赤脚**的时候才会不怕**穿鞋的**，看到很多同胞还在害怕所谓的“*上征信*”而还在硬撑着不敢断供并继续选择当冤大头时很是痛心，其实我国明面上还是一个法制国家，大多数情况下还是有理可说的，故在本项目下的 `相关法律与审判案例支持.md` 文件里放上相关的成功审判案例与法律依据供同胞们学习与了解。
另外，本人是互联网从业人员，并非法律专业人员，欢迎相关专业人士参与修改与补充！

文章链接：[相关法律与审判案例支持](相关法律与审判案例支持.md)

## PR 相关

### 如何创建 PR，并为本项目做贡献

鉴于很多人对于 Git 较为生疏，这里就写上一篇文章来尽可能降低大家发 PR 为本项目增加信息的门槛，只需要一个浏览器即可完成操作。

文章链接：[如何为本项目提交信息](如何为本项目提交信息.md)

### PR 基本格式规范

> 注意，目前我们约定：
> 如果一个楼盘有多张图片作为支撑材料，则在该省份/城市文件内再新建一个以该楼盘命名的文件夹存放，并加上"_"前缀以示区别，例如`images/广西/桂林/_桂林融创文旅城N4地块`，其下存放了两张图片，否则无法通过本地图片验证脚本[validateLocalImages.ts](development/backend/validateLocalImages.ts)

- 1、新增项目信息，请务必修改 `README.md` 文件，以及修改全国、省、市总数！否则不予通过
- 2、必须附有图片等证明
- 3、请记得检查是否需要解决冲突
- 4、删除项目信息请提供复工图片，并上传至 `images` 文件夹相对应的省份

## 开发相关

[**--> 开发指引**](./development/README.md)

### 数据校验工作

- [x] 基于CI，[analyze.ts](development/backend/analyze.ts)已实现每次 push 对 readme 文档中的计数（包括城市、省份、合计）、图片链接的有效性自动进行校验
- [x] [validateLocalImages.ts](development/backend/validateLocalImages.ts)已实现对 images 文件夹中图片在文档中的引用进行核验（确保没有游离的图片）

## 数据概要

### 总计【298+】

<details>
<summary>可视化（Silver）</summary>
<img src="data/generated/visualization-light.png" alt="visualization-light">
</details>

<details>
<summary>可视化（Dark）</summary>
<img src="data/generated/visualization-dark.png" alt="visualization-dark">
</details>

全国总数便携计算代码（F12 打开 console，复制回车即可）：

```js
let i = 0;
[...$('.markdown-body').childNodes].forEach(item => {
    if (item.nodeName === 'H3') {
        const n = item.textContent.match(/\[\s*(\d+)\s*\]/)
        i += Number(n && n[1])
    }
})
console.log(i)
```

### 结构化数据 （基于本 README 文档生成）

- [数据：基于楼盘的停贷数据](data/generated/properties.json)（含省市区、链接、月份）
- [数据：基于城市的停贷数据](data/generated/cities-for-visualization.json) （含省市区、楼盘统计数、经纬度）
- [数据：全国三级行政城市经纬度数据](data/source/region-tree.json)

### 其他数据公示处

```txt
项目发起人：被 ban 了

我来文档：https://www.wolai.com/xutejcDgz9B3aTcrRCjxB1

Notion 数据库：https://www.notion.so/21dab14200e2478eb91c49b68d16495f
```

## 分省数据（按拼音排序）

### 安徽省 [ 2 ]

- **合肥市（2）：** 恒大中心（8月），斯瑞大厦

### 北京市 [ 3 ]

- **通州区（1）：** [禹洲朗廷湾（朗廷雅苑）](images/北京/北京禹洲朗廷湾.jpeg)
- **石景山区（1）：** [禧悦学府（悦创佳苑）](images/北京/禧悦学府.jpeg)
- **朝阳区（1）：** [上东郡（澜悦景苑）](images/北京/澜悦景苑.jpeg)

### 重庆 [ 13 ]

- **渝北区（5）：** [阳城未来悦二期（7月）](images/重庆/阳城未来悦二期.jpg)，[融创隐溪晓院一二三期](images/重庆/重庆市渝北区融创隐溪晓院全体业主强制停贷预告书.png)，蓝光未来城，恒大轨道时代二期，芙蓉公馆（9月）
- **黔江区（2）：** 恒大名都（7月），富力院士延琅境
- **沙坪坝区（1）：** [佳兆业·凤鸣水岸（9月）](images/重庆/重庆_佳兆业凤鸣水岸.jpg)
- **万州区（2）：** 万萃城二期（12月），万萃城二期（12月）
- **巴南区（2）：** 恒大新城四期，[世茂·江城铭著](images/重庆/世茂江城铭著.jpg)
- **璧山区（1）：** [璧山区融创城（9月）](images/重庆/重庆_璧山_融创城.jpg)

### 福建省 [ 2 ]

- **福州市（2）：** [天泽奥莱时代（8月）](images/福建/福州市奥莱时代.jpg)，恒大天璟二期

### 甘肃省 [ 2 ]

- **兰州市（1）：** [兰州新区绿地智慧金融城六期康养谷](images/甘肃/兰州新区绿地智慧金融城六期康养谷.jpeg)
- **庆阳市（1）：** 国金one（11月）

### 广东省 [ 7 ]

- **广州市（1）：** [万科海上明月（9月）](images/广东/gz001.png)
- **深圳市（3）：** [佳兆业樾伴山](images/广东/sz001.jpg)，佳兆业时代大厦，[前海天境花园](images/广东/sz003.jpg)
- **汕头市（1）：** 恒大金碧外滩湾（八月）
- **中山市（1）：** 泰禾金尊府
- **揭阳市（1）：** 恒大翡翠华庭二期

### 广西壮族自治区 [ 16 ]

- **南宁市（9）：** 五象澜庭府臻苑，[五象澜庭府沁苑](images/广西/南宁/南宁市五象澜庭府沁苑.png)，蓝光雍锦澜湾，江宇世纪公馆，融创融公馆11、12号楼（8月），金科博翠山，[东鼎雍和府（9月）](images/广西/南宁/南宁东鼎雍和府.png),[中鼎公园府](images/广西/南宁/广西省南宁市中鼎公园府全体业主强制停贷告知书.png)，[南宁恒大华府二期](images/广西/南宁恒大华府二期告知书.png)
- **梧州市（1）：** [恒大绿洲二期（8月）](images/广西/梧州恒大二期停贷.png)
- **桂林市（4）：** [融创文旅城N7地块（10月）](images/广西/桂林/桂林融创N7.png)，[桂林融创文旅城N4地块](images/广西/桂林/_桂林融创文旅城N4地块)，灵川汇金万象新城（11月），[桂林恒大城（10月）](images/广西/桂林/桂林恒大城.jpg)
- **玉林市（1）：** 中鼎绿地中心
- **钦州市（1）：** 恒大御景半岛二期

### 贵州省 [ 2 ]

- **贵阳市（2）：** 中天吾乡，中环国际阅湖

### 河北省 [ 20 ]

- **石家庄市（5）：** 恒润中央广场，恒大悦龙台，恒大时代新城（8月），[安联生态城凯旋府](images/河北/石家庄/石家庄市安联生态城凯旋府全体货款业主强制停货告知书.jpeg), [石家庄赫石府](images/河北/石家庄/石家庄市赫石府全体货款业主强制停货告知书.png)
- **邯郸市（1）：** [恒大悦珑湾](images/河北/邯郸/邯郸恒大.jpg)
- **廊坊市（5）：** 鸿坤理想城，鸿坤凤凰城五期（8月），盈时·未来港，[华夏幸福·四季公馆](images/河北/廊坊/河北廊坊市大厂回族自治县四季公馆强制停贷告知书.jpeg)，华夏幸福孔雀城大运河智慧街区（香河）
- **邢台市（2）：** 恒大悦府，永康万国城
- **承德市（1）：** 状元府
- **张家口市（2）：** 宣化恒大滨河左岸，宣化恒大翡翠湾
- **保定市（3）：** 上东御景，[隆基泰和涿州铂悦山](images/河北/保定/隆基泰和涿州铂悦山项目全体业主强制停贷告知书.jpeg)，[隆基泰和紫悦小区](images/河北/保定/涿州市隆基泰和紫悦小区.jpeg)
- **沧州市（1）：**[紫樾香榭](images/河北/沧州/沧州市紫樾香榭全体业主强制停贷告知书.jpeg)

### 河南省 [ 59 ]

- **郑州市（39）：** 名门翠园，瀚海思念城，康桥玖玺园，奥园悦城（汇景园），龙湖锦艺城高六，啟福城，[郑州鑫苑国际新城](images/河南/郑州鑫苑国际新城.jpg)，[鑫苑名城3号院住宅](images/河南/郑州鑫苑名城3号院住宅项目.png)，郑西鑫苑名家四期（7月），名门天境，正商玖号院，名门紫园，恒大养生谷，锦艺轻纺四期未来公寓，康桥阅溪雅苑，康桥香溪郡，清华城（7月），[豫发白鹭源春晓三期](images/河南/郑州航空港区豫发白鹭源春晓三期全体业主停贷告知书.jpg)（8月），华纳龙熙湾，康桥未来公元，奥园御湖城，恒大城，绿地城二区（7月），[融创中原大观二期](images/河南/郑州市融创中原大观二期停贷告知书.png)（10月），绿地滨湖国际城，盛润城壹号公馆，绿地溱水小镇，永恒理想世界三期（9月），龙湖一号（9月），[蓝宝桃源里](images/河南/蓝宝桃源里全体业主强制停贷告知书.png)，[泰山誉景朗誉园](images/河南/泰山誉景全体业主决定于2022年9月强制停贷告知书.jpeg)（9月），[鑫苑金水观城](images/河南/郑州市鑫苑金水观城.jpg)，[金水区康桥东麓园二期](images/河南/郑州市金水区康桥东麓园二期全体业主于2022年10月1日强制停贷告知书.jpeg)（10月）,[孔雀城公园海](images/河南/郑州孔雀城公园海.png)，浩创梧桐茗筑（7月），康桥那云溪（8月), [九裕龙城](images/河南/九裕龙城.jpeg)（8月），[威龙尚品号楼（10月底三期三年停贷）](images/河南/郑州新郑威龙尚品13号楼全体业主强制停贷告知书.jpeg)，[郑州新田城湖光里二期(原洞林文苑)](images/河南/郑州新田城湖光里二期（原洞林文苑）.jpg)
- **新乡市（2）：** 平原新区恒大三期半城湖（8月），[新乡市豫飞盛世城邦（8月）](images/河南/新乡豫飞盛世城邦.jpg)
- **南阳市（3）：** 阳光城丽景花园，兴达珑府，恒大御府
- **漯河市（1）：** 恒大悦府
- **商丘市（2）：** 恒大名都二期，名门城五期
- **驻马店市（5）：** [恒大悦府](images/河南/驻马店恒大悦府.png)，佳和新城，平舆县琥珀蓝岸（10月），中原城，遂平县绿地苑
- **荥阳市（1）：** 居易西郡
- **许昌市（2）：** 融创观河宸院，金科鹿鸣帝景
- **洛阳市（1）：** 恒大云湖上郡
- **安阳市（2）：** 恒大悦府，紫薇公馆
- **周口市（1）：** 槐府六号三期

### 湖北省 [ 28 ]

- **武汉市（17）：** [恒大时代新城（8月）](images/湖北/武汉/恒大时代新城.png)，[绿地光谷星河绘](images/湖北/武汉/绿地光谷星河绘.jpg)，[人福国际健康城（7月）](images/湖北/武汉/人福国际健康城.png)，[恒大科技城（8月）](images/湖北/武汉/恒大科技旅游城.png)，[美好香域花境](images/湖北/武汉/美好香域花境.jpg)，当代铭山筑，君悦花园（知音湖院子），[奥山首府，奥山经开澎湃城（7月）](images/湖北/武汉/奥山首府（奥山郡）.png)，绿地光谷中心城，[奥山汉口澎湃城](images/湖北/武汉/武汉东西湖奥山汉口澎湃城.jpg)，[汉南绿地城二期](images/湖北/武汉/汉南绿地城二期.png)，[光谷绿地中心城JKL地块](images/湖北/武汉/光谷绿地中心城JKL地块.png)，泰禾知音湖院子，[恒大龙城四期](images/湖北/武汉/恒大龙城四期.png)，新洲中新盛景，[奥山首府（奥山郡](images/湖北/武汉/奥山首府（奥山郡）.png)
- **鄂州市（3）：** 恒大童世界四号地（廊桥水乡）（9月） ，鄂州市花样年香门第，恒大文化旅游城
- **随州市（1）：** 恒大悦龙台 （10月）
- **咸宁市（3）：** 联乐广场，绿地城际空间站，恒大名都
- **荆门市（1）：** 实地紫薇雅著
- **襄阳市（2）：** 恒大翡翠龙庭一期（8月），蓝光雍锦园
- **孝感市（1）：** 润达·壹号广场

### 湖南省 [ 29 ]

- **长沙市（10）：** [恒泰芙蓉悦府](images/湖南/湖南省长沙市恒泰芙蓉悦府全体业主停贷告知书.jpg)，恒大滨江左岸，合能枫丹宸悦，合能湘江公馆，长沙文景，恒大御景天下二期（8月），恒大悦湖商业广场（12月），滨江正荣紫阙台，[宁乡未来方舟2期&3期](images/湖南/宁乡未来方舟.jpg)，新力铂园（8月）
- **邵阳市（1）：** 恒大华府（9月）
- **岳阳市（1）：** 恒大未来城二期（8月）
- **衡东县（1）：** 奥体公馆
- **湘潭市（4）：** 恒大书香门第15、16栋，[和达滨江公园](images/湖南/湘潭市和达滨江花园强制停贷书.jpg)，湘台国际花园二期，[金奥湘江公馆](images/湖南/湘潭金奥湘江公馆一二期停贷告知函.jpg)
- **怀化市（2）：** 恒大中央广场（8月），恒大帝景
- **株洲市（6）：** 诚建檀香山，北大资源翡翠公园，绿地城际空间站，[华晨金水湾三四期](images/湖南/湖南株洲.jpg)，华晨神农湾，东成中心1栋
- **衡阳市（1）：** 华源北街
- **永州市（2）：** 舜德湘江，道县东方丽都三期（永州道县）
- **浏阳市（1）：** 恒大华府四期

### 吉林省 [ 1 ]

- **公主岭市（1）：** 恒大花溪谷或水世界

### 江苏省 [ 12 ]

- **宿迁市（1）：** 恒大悦澜湾
- **靖江市（1）：** 恒大御景半岛
- **镇江市（2）：** 恒大童世界，宝华泰禾金尊府
- **南京市（1）：** 金陵华夏中心（8月）
- **苏州市（2）：** [泰禾金尊府（8月)](images/江苏/苏州泰禾金尊府.jpg)  ，[阳光城檀苑](images/江苏/苏州阳光城檀苑.jpg)
- **常州市（2）：** 三盛璞悦湾，[句容-泰禾金尊府](images/江苏/常州/句容-泰禾金尊府.JPG)
- **无锡市（1）：** 天渝骄园
- **南通市（1）：** 阳光城未来悦
- **扬州市（1）：** [恒大观澜府](images/江苏/扬州恒大观澜府.jpg)

### 江西省 [ 14 ]

- **景德镇市（3）：** 恒大珑庭，恒大翡翠华庭，恒大悦府
- **南昌市（5）：** 新力城，鸿海城（10月），恒大珺庭（8月），中金中心，恒大林溪府（10月）
- **新余市（1）：** 恒大翡翠华庭（9月）
- **宜春市（1）：** 恒大绿洲四期
- **赣州市（2）：** 绿地博览城，[于都县恒大御景北区](images/江西/赣州市于都县恒大御景北区业主强制停贷告知书.png)
- **萍乡市（2）：** 恒大御府二期，庄和中央华府（10月）

### 辽宁省 [ 7 ]

- **沈阳市（5）：** 恒大西江天悦，[恒大中央广场](images/辽宁/沈阳恒大中央广场.jpg)，恒大时代新城，金科集美东方，[恒大盛京珺庭](images/辽宁/沈阳恒大盛京珺庭.png)
- **大连市（2）：** [融创海逸长洲](images/辽宁/大连融创海逸长洲.jpg) ，香海滨城二期

### 内蒙古自治区 [ 1 ]

- **呼和浩特市（1）：** 香墅岭西区（10月）

### 山东 [ 10 ]

- **青岛市（7）：** [三盛国际海岸五期（9月）](images/山东/青岛/三盛国际.jpeg)，[绿地城际空间站（9月）](images/山东/青岛/绿地城际空间站.png)，[实地蔷薇国际](images/山东/青岛/实地蔷薇国际.jpeg)，[胶州协信天骄云麓](images/山东/青岛/胶州协信天骄云麓.jpeg)， [黄岛蓝光雍锦半岛（6月)](images/山东/青岛/蓝光雍锦半岛.jpeg)， [中南林樾小区（7月）](images/山东/青岛/李沧中南林樾.jpg)，[西海岸新区世茂•香奈公馆（10月）](images/山东/青岛/青岛西海岸新区世茂•香奈公馆.jpeg)
- **济南市（2）：** [阳光城檀悦](images/山东/济南/阳光城檀悦.jpeg)，[融创中新国际城四期南区](images/山东/济南/融创中新国际城四期南区.jpeg)
- **烟台市（1）：** [松隽阳光城（12月）](images/山东/烟台/松隽阳光城.jpeg)

### 山西省 [ 10 ]

- **太原市（10）：** 泰禾金尊府，[太原富力天禧城3期](images/山西/太原市富力天禧城3期.jpg)，[太原市恒大御景湾4期](images/山西/太原市恒大御景湾4期.jpg)，宝能城一期（8月），恒大金碧天下八期（10月），[绿地新里城二期](images/山西/太原绿地新里程.jpg)，恒大金碧天下五期（八月），[太原市融创中心](images/山西/太原市融创中心.png)，[恒大森林海一期](images/山西/太原/太原恒大森林海一期全体业主强制停贷告知书.jpeg)，[恒大滨河府二期](images/山西/太原/太原恒大滨河府二期全体业主决定千2022年9月强制停贷告知书.jpeg)

### 陕西省 [ 21 ]

- **西安市（20）：** [世茂璀璨倾城二期](images/陕西/西安/西安世茂璀璨倾城二期停贷告知书.png)，正荣紫阙台，[正荣紫阙峯著](images/陕西/西安/西安正荣紫阙峯著全体业主强制停贷告知书.png)，[绿地新里程三期兰亭公馆](images/陕西/西安/西安绿地兰亭公馆全体业主强制停贷告知书.png)，德杰状元府邸（9月），阳光100阿尔勒（8月），[西安康桥悦蓉园（9）](images/陕西/西安/西安康桥悦蓉园13号楼停贷告知函.png)，绿地璀璨天城二期，乐华城香榭庄园 ，[当代嘉宝公园悦](images/陕西/西安/当代嘉宝公园悦停贷告知书.png)，西安铭鸿中心二期，[锦业6号府邸](images/陕西/西安/西安锦业6号府邸停贷通知书.png)，[万和郡](images/陕西/西安/西安万和郡停贷告知.png) ，鄠邑区名仕华庭，[西安当代境MOMA](images/陕西/西安/西安当代境MOMA项目预停贷告知书.png)，国际幸福城，[西安名京院望](images/陕西/西安/西安名京院望停贷告知书.jpg)，[西安沣东新城君合天玺](images/陕西/西安/西安沣东新城君合天玺.jpeg)，西安灞桥区易合坊，[西安恒大文化旅游城（8月）](images/陕西/西安/西安恒大文化旅游城强制停贷告知书.jpeg)
- **咸阳市（1）：** [融创御河宸院DK6](images/陕西/咸阳/咸阳融创御河宸院DK6全体业主停货告知书.png)

### 上海 [ 5 ]

- **崇明区（1）：** [崇明长兴岛泰禾大城小院](images/上海/Xingdao_Shanghai.png)
- **嘉定区（1）：** [徐行佳兆业五期](images/上海/上海徐行佳兆业五期.jpeg)
- **浦东新区（2）：** [临港万祥颐景园江南院](images/上海/上海临港万祥颐景园江南院.jpeg)，[上海浦东新区君御公馆](images/上海/上海浦东新区君御公馆停贷通知书.png)
- **奉贤区（1）：** [上海市奉贤区泰禾海上院子](images/上海/上海市奉贤区泰禾海上院子.jpg)

### 四川省 [ 16 ]

- **成都市（9）：** [恒大牧云天峰（8月）](images/四川/成都新津恒大牧云天峰.jpg)，[恒大未来城4期（7月）](images/四川/成都市温江区恒大未来城4期.jpg)，[武侯新城当代璞誉（7月）](images/四川/whxcdd.jpg)，[新尚尚院（10月）](images/四川/成都温江区新尚尚院告知书.png)，置信逸都城（9月），阳光城未来悦 ，[恒大林溪郡（8月）](images/四川/hdlxj.jpg)，[三盛翡俪山（8月）](images/四川/ssfls.jpg)，[万锦熙岸2期（8月）](images/四川/wjxa2.png)
- **泸州市（1）：** 恒大翡翠湾
- **眉山市（1）：** 恒大文化旅游城（10月）
- **都江堰市（1）：** 融创文旅滨江新区（8月）
- **德阳市（1）：** 恒大翡翠华庭
- **广安市（1）：** 帝谷公园城三期
- **巴中市（1）：** 恩阳川旅世纪外滩
- **眉山市（1）：**[眉山市彭山区融创水郡未来城（江口水镇）（10月）](images/四川/眉山市彭山区融创水郡未来城、江口水镇全体业主决定强制停贷告知书.png)

### 天津市 [ 8 ]

- **天津城区（3）：** 实地海棠雅著圣景豪庭（8月），实地蔷薇（9月），融创南开宸院二期
- **北辰区（2）：**[融创津宸壹号](images/天津/天津市津宸壹号全体业主“动态还贷”告知书.png)，[融创御景宸院](images/天津/天津市北辰区融创御景宸院全体业主强制停贷告知书.png)（10月）
- **武清区（1）：** 恒大翡翠湾（10月）
- **津南区（1）：** 四季春晓
- **宝坻区（1）：** [宝坻区实地海棠雅著圣景豪庭](images/天津/天津市实地海棠雅著圣景豪庭.jpeg)

### 云南省 [ 7 ]

- **昆明市（6）：** 恒大城（9月），蓝光德商天域（8月），恒大阳光半岛（9月），恒大玖珑湾（9月），佳兆业城市广场（9月），实地花鹤翎（10月）
- **玉溪市（1）：** 樱花谷（7月）

### 浙江省 [ 3 ]

- **杭州市（3）：** [中润璞玉公馆](images/浙江/杭州/中润璞玉公馆.png)，[富阳区泰禾大城小院楼盘](images/浙江/杭州/浙江省杭州市富阳区泰禾大城小院楼盘富政储出（2010）20号地块购房者暂停还货告知书.jpg)，[杭州中南春溪集](images/浙江/杭州/浙江杭州中南春溪集.png)
