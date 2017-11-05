# tableHeaderFixed
一个滚动表头固定顶部的jQuery插件，支持页面固定及容器内固定

# Demo
见文件 `./index.html` 

![Demo](https://github.com/imwtr/jquery-tableHeaderFixed/blob/master/test.gif)


# 如何使用
默认参数选项
```javascript
       {
            // 表头在页面滚动时固定在头部
            fixedInPage: true,
            // 表头在容器滚动时固定在容器头部
            fixedInContainer: false,
            // 表格容器最大高度 当fixedInContainer为true时生效
            containerMaxHeight: 400,
            // 容器类名
            containerClass: 'table-fixed-content-wrap',
            // 固定表头的类名
            fixedHeaderClass: 'table-fixed-header'
        };

```
需要设置固定表头类名为初始隐藏
```css
  .table-fixed-header {
      display: none;
  }
```

默认设置为固定于页面顶部
```javascript
  $('.page-table-test').find('tbody').html(getHtml(dataTpl, data))
       .end().tableHeaderFixed();
```

自定义设置为固定于容器里
```javascript
  $('.content-table-test').find('tbody').html(getHtml(dataTpl, data))
      .end().tableHeaderFixed({
           fixedInContainer: true,
           containerMaxHeight: 300
      });
```

