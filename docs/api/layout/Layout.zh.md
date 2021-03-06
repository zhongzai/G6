---
title: Layout
order: 0
---

在 G6 中使用布局，在实例化图时配置 `layout` 属性。例如：
```javascript
const graph = new G6.Graph({
  ...                      // 其他配置项
  layout: {                // Object，可选，布局的方法及其配置项，默认为 random 布局。
    type: 'force',
    preventOverlap: true,
    nodeSize: 30,
    ...                    // 其他配置
  }
});
```

每种布局方法的配置项不尽相同，具体参见本目录下每种布局的 API。<br />当实例化图时没有配置 `layout` 时：

- 若数据中节点有位置信息（`x` 和 `y`），则按照数据的位置信息进行绘制；
- 若数据中节点没有位置信息，则默认使用 Random Layout 进行布局。

以下方法为自定义布局时可能需要复写的方法。如果非自定义，使用内置布局方法时，以下方法由 G6 控制并调用，用户不需要了解。


## 初始化

### init(data)
初始化布局。


**参数**

| 名称 | 类型 | 是否必选 | 描述 |
| --- | --- | --- | --- |
| data | object | true | 布局中使用的数据 |



### getDefaultCfg()
返回布局的默认参数。

**返回值**

| 名称 | 类型 | 是否必选 | 描述 |
| --- | --- | --- | --- |
| cfg | object | true | 布局的默认参数 |



## 布局

### execute()
执行布局算法。


### layout(data)
根据传入的数据进行布局。


**参数**

| 名称 | 类型 | 是否必选 | 描述 |
| --- | --- | --- | --- |
| data | object | true | 布局中使用的数据 |



## 更新

### updateCfg(cfg)
更新布局参数。


**参数**

| 名称 | 类型 | 是否必选 | 描述 |
| --- | --- | --- | --- |
| cfg | object | true | 新的布局配置 |



## 销毁

### destroy()
销毁布局。
