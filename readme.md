
### react图片引入方式

```
import testImg from 'imageRoot/test.png'

<img alt="404" src={ testImg } />
```

#### react 样式
```
style={{display: this.props.hasName ? 'block' : 'none'}}

className={classnames({ 'list-action': this.state.hot })}
```

### 判断组件渲染

```
let list = null
if (this.props.home.hotListShow) {
  list = (<Hot {...this.props} />)
} else {
  list = (<Coming {...this.props} />)
}

{list}
```

#### react 点击事件传递参数

```
<button onClick={() => {this.handleClick(ev, par, par2)}}></button>

handleClick(porps0, props1, ..., event) {
    // your code here
}

```

### react fetch post， 上传图片请求时的坑

```
[参考文章](http://blog.csdn.net/codetomylaw/article/details/52446786)
```

#### 路由跳转传递参数

```
 1.
    import { Link } from 'react-router'
     <Link to={`/cinema/${item.id}`}购买 </Link>
 2.
   import { History } from 'react-router'
   this.props.history.push('/payfor/2')  
```

### react 路由跳转
```
  router.push('/no')
```

#### 获取url参数id

`this.props.params.id`


### react 父组件给子组件传值

```
<Search {...this.props} />
```

### react package.json 中设置代理解决跨域问题

```
安装中间件 http-proxy-middleware

```
### reacdt a标签，img标签写法

```
<a href={'tel:'+this.state.lists.phone} className='phone'></a>
<img src={require('../assets/phone.svg')} />
```

```
https://segmentfault.com/a/1190000008635891
```
[reduce---applyMiddleware](http://cn.redux.js.org/docs/api/applyMiddleware.html)
[react-route4](http://react-china.org/t/react-router4/15843)


### 解决iponex下刘海问题
```
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
viewport-fit=cover 这个属性使iphonex没有白边，占满屏幕
```

### rimraf

**rimraf 包的作用：以包的形式包装rm -rf命令，就是用来删除文件和文件夹的，不管文件夹是否为空，都可以删除。**
[参考文章](https://segmentfault.com/a/1190000011831802)



####  Chrome 开发工具

[react]( https://cdn.deliciousbrains.com/content/uploads/2017/06/15151112/react-devtools.mp4)

[vue]( https://cdn.deliciousbrains.com/content/uploads/2017/06/15151111/vue-devtools.mp4)


### 启动vpn

vpn cd -->
/home/mac/OpenVPN/config

```
sudo openvpn test.ovpn
```

