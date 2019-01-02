1、输入url回车
2、浏览器查看当前url是否具有缓存
3、dns域名解析
4、建立tcp链接(http3次握手)
5、发送http请求
6、浏览器收到响应，渲染DOM节点
7、关闭tcp链接 (4次挥手)


拓展问题
 跨域【不同源策略】
	https://www.jianshu.com/p/438183ddcea8
 浏览器缓存
	https://github.com/amandakelake/blog/issues/41
 浏览器响应常用状态码
	https://blog.csdn.net/laishaohe/article/details/79052085
	列举
	  200 请求成功
	  301 302 请求的资源移动到新的位置
	  304 请求资源未修改，可以继续使用以前的数据
	  400 客户端请求语法错误，服务器端不理解
	  401 请求需要身份认证
	  403 请求拦截
	  404 请求资源路径不存在
	  500 服务器内部错误
	  505 服务器不支持HTTP协议版本
 页面渲染
	https://segmentfault.com/a/1190000010298038
	1、通过HTML Parser将HTML标签解析成DOM Tree
	2、通过CSS Parser将CSS解析成CSSDOM树
	3、通过render将俩者渲染成Render Tree
	4、通过Layout计算出每个DOM节点的信息【回流/重排 reflow】
	5、通过Painting将计算好的信息绘制整个页面【repaint重绘】

	什么时候触发重排？什么时候会触发重绘？
	  1、增加、删除、修改DOM结点时，会导致Reflow
	  2、移动DOM的位置，或是搞个动画的时候会导致Reflow
	  3、修改网页的默认字体时会导致Reflow
	  4、修改样式背景颜色、背景图片、边框的时候会导致Repaint

	只要触发Reflow一般都会触发Repaint
	