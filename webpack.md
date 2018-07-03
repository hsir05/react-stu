

### 1.webpack 代码gzip压缩、注释、警告去除配置，设置缓存

#### 1.1 代码gzip压缩 去掉注释 忽略警告

```
new webpack.optimize.UglifyJsPlugin({ // gzip压缩comments: false,        //去掉注释
  comments: false,        //  去掉注释
  compress: {
    warnings: false   //  忽略警告,要不然会有一大堆的黄色字体出现……
  }
})
```

#### 1.2  react打包去掉.map文件

**map文件是帮助我们查看报错的位置的。**

```
map文件由devtool属性控制，如果不想要map，注释掉就可以，大约webpack.config.prod.js第57行；
```
```
devtool: shouldUseSourceMap ? 'source-map' : false,
```

[参考文章1](https://www.jianshu.com/p/a64735eb0e2b)
[参考文章2](https://segmentfault.com/a/1190000007892189)
[参考文章3](https://blog.csdn.net/bbsyi/article/details/78781933)


### 2.移动前端调试方案（Android + Chrome 实现远程调试）

`chrome://inspect/#devices`

[参考文章1](http://www.cnblogs.com/leinov/p/4094138.html)

