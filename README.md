
## 移动端使用后flex布局，对付天朝机子要写好多兼容css，要是定样式的地方都写得的话非常恶心，这里我们介绍sass工具还快速帮我写兼容


**混合宏-调用混合宏**

在 Sass 中通过 @mixin 关键词声明了一个混合宏

```
@mixin flex-direction-column-reverse {
        -webkit-box-pack: end;
        -webkit-box-direction: reverse;
        -webkit-box-orient: vertical;
        -moz-flex-direction: column-reverse;
        -webkit-flex-direction: column-reverse;
        flex-direction: column-reverse;
}

 ```
在实际调用中，其匹配了一个关键词“@include”来调用
```
 button {
     @include flex-direction-column-reverse;
}
```
这个时候webstrom 编译出来的 CSS: **暴爽有没有，跟恶心说拜拜**
```
 button {
        -webkit-box-pack: end;
        -webkit-box-direction: reverse;
        -webkit-box-orient: vertical;
        -moz-flex-direction: column-reverse;
        -webkit-flex-direction: column-reverse;
        flex-direction: column-reverse;
 }
```
