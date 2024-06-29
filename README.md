![](https://i1.mcobj.com/imgb/u18prz/20240629_66801e5dd281f.png)

# Map-of-Graduation-Direction

A visual distribution map of graduation destinations, using AMAP API.

## 一个可视化的毕业去向分布地图，使用了高德地图API。

技术不佳，文档翻遍。东改西改，代码凌乱。

### 特征介绍

- 良好的跨平台支持。
- 信息修改便捷。
- 支持点击信息列表快速跳转对应位置。
- 界面简洁美观。

### 相关信息

对于可变内容，修改 `data\v1\schoolInfo` 即可。

本分支修改了以下内容：

- 修改信息分类方式：现在采取院校组合模式，信息窗口更清晰。
- 重写信息窗口和位置标注部分，规避高德地图低限额API。（高德你现在怎么连静态地图都有限额了。。。）
- 导航搜索和跳转功能优化。

- 新的信息格式如下：

```
{
        id: "NKU",// 每院校组唯一ID
        displayName: "南开大学（八里台校区）", // 显示在悬浮窗口和人员列表的名称
        lng: "117.167328",// 经纬度，可以登陆账号后从https://lbs.amap.com/tools/picker获取
        lat: "39.103715",
        students: [// 学生信息
            {name:"学生甲", major:"法学"},
            {name:"学生乙", major:"工科试验班（信息计算科学）"}
        ]
}
```

![](https://img.picui.cn/free/2024/06/29/66802150e8a91.png)
