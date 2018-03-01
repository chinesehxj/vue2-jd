# Vue2-jd


一个使用了基于vue2 + mintUI + vuex + asxio + sass 构建的高仿京东IOS风格的App大型商城网站,目前基础功能基本完成，后续将会持续更新添加新功能...

该项目是一个前后端分离项目，前后端全栈开发。后端api又和管理系统分开使用。api使用了基于node.js的express来做接口的开发。管理系统则使用了element-damin搭建。对应传送门请看下面

__本项目纯属个人瞎弄，正常购买商品请选择京东官方App__

## 对应的后台项目

- [node-api-jd](https://github.com/Caitingwei/node-api-jd)

- [node-admin-jd](https://github.com/Caitingwei/node-admin-jd)

>  如果对您有帮助，您可以点右上角 "Star" 支持一下 谢谢(~~求你了~~)

# 演示

[查看demo请戳这里](http://awei.fun/mobile)（请用chrome手机模式预览）

[后台管理系统请戳这里](http://awei.fun/admin)（请用chrome手机模式预览）

### 移动端扫描下方二维码

<img src="https://github.com/Caitingwei/vue2-jd/blob/master/qrcode.png" width="250" height="250"/>


## 效果展示

- 响应式布局首页
![image](https://github.com/Caitingwei/vue2-jd/blob/master/home.png)

- 底部商品推荐
![image](https://github.com/Caitingwei/vue2-jd/blob/master/home2.png)

- 顶部搜索栏
![image](https://github.com/Caitingwei/vue2-jd/blob/master/search.png)

- 商品详情页
![image](https://github.com/Caitingwei/vue2-jd/blob/master/product.png)

- 文章资讯
![image](https://github.com/Caitingwei/vue2-jd/blob/master/article2.png)

- 视频资讯
![image](https://github.com/Caitingwei/vue2-jd/blob/master/article.png)

- 文章详情
![image](https://github.com/Caitingwei/vue2-jd/blob/master/articleDetail.png)

- 用户登录
![image](https://github.com/Caitingwei/vue2-jd/blob/master/login.png)

- 注册
![image](https://github.com/Caitingwei/vue2-jd/blob/master/zhuci.png)

- 购物车
![image](https://github.com/Caitingwei/vue2-jd/blob/master/cart.png)

- 下单
![image](https://github.com/Caitingwei/vue2-jd/blob/master/createOrder.png)

- 下单-支付密码
![image](https://github.com/Caitingwei/vue2-jd/blob/master/createOrder2.png)

- 订单列表
![image](https://github.com/Caitingwei/vue2-jd/blob/master/orderList.png)

- 评价
![image](https://github.com/Caitingwei/vue2-jd/blob/master/pingjia.png)

- 个人中心
![image](https://github.com/Caitingwei/vue2-jd/blob/master/usercenter.png)

- 设置中心
![image](https://github.com/Caitingwei/vue2-jd/blob/master/sz.png)

## 安装

#### 注意：由于涉及大量的 ES6/7 等新属性，node 需要 6.0 以上版本 

```
git clone https://github.com/Caitingwei/vue2-jd.git

cd vue2-jd

//这里使用淘宝镜像安装能快一点
npm --registry https://registry.npm.taobao.org install

```
## 运行

### 本地调试模式

```
npm run start

```
### 生产模式(部署)

```
npm run build

```

# 项目布局

```
.
├── build                                       // webpack配置文件
├── config                                      // 项目打包路径
├── dist                                        //上线项目文件npm run build后生成放在服务器即可正常访问
├── screenshots                                 // 项目截图
├── src                                         // 源码目录
│   ├── components                              // 组件
│   │   ├── common                              // 公共组件
│   │   │   ├── marquee                         //广播轮播组件
│   │   │   ├── backHead.vue                    // 返回顶部组件
│   │   │   ├── loadMore.vue                    // 加载更多上拉刷新组件
│   │   ├── footer
│   │   │   └── footerView.vue                  // 底部公共组件
│   ├── config                                  // 基本配置
│   │   ├── div.env.js                          // 本地开发环境配置
│   │   ├── prod.env.js                         // 生产模式环境配置
│   │   └── index.js                            // 根文件
│   ├── assets                                  // 公共资源文件
│   ├── page
│   │   ├── chat                                // 消息聊天 （还未开发）
│   │   ├── cms                                 // 资讯类模块
│   │   │   ├── index.vue                       // 首页
│   │   │   ├── article.vue                     // 咨询列表
│   │   │   └── articleDetail.vue               // 咨询详情
│   │   ├── member
│   │   │   ├── addressList.vue                 // 地址列表
│   │   │   ├── address.vue                     // 编辑、新增地址
│   │   │   ├── forget.vue                      //  忘记密码
│   │   │   ├── login.vue                       // 登录
│   │   │   ├── myhome.vue                      // 个人中心
│   │   │   ├── register.vue                    // 注册
│   │   │   └── sttings.vue                     // 设置
│   │   └── shop
│   │       ├── cart.vue                        // 购物车
│   │       ├── category.vue                    // 商品分类
│   │       ├── createOrder.vue                 // 创建订单
│   │       ├── order.vue                       // 订单详情
│   │       ├── orderList.vue                   // 订单列表
│   │       ├── product.vue                     // 商品详情
│   │       ├── review.vue                      // 评价
│   │       ├── searchBar.vue                   // 顶部搜索栏+搜索
│   │       ├── searchRusult.vue                // 搜索结果列表页
│   │       └── shop.vue                        // 店铺详情
│   ├── plugins                                 // 引用的插件
│   │   └── flexible.js                         // rem相关配置
│   ├── router
│   │   └── index.js                            // 路由配置
│   ├── service                                 // 数据交互统一调配
│   │   └── getData.js                          // 获取数据的统一调配文件
│   ├── store                                   // vuex的状态管理
│   │   ├── modules                             // 配置actions,相关接口请求都在actions中进行
│   │   │   ├── app.js                          // app模块相关的数据
│   │   │   ├── cms.js                          // cms模块相关的数据
│   │   │   ├── shop.js                         // shop模块相关的数据
│   │   │   └── user.js                         // user模块相关的数据
│   │   ├── getter.js                           // 全局计算属性数据
│   │   └── index.js                            // 初始化全局Vuex
│   └── utils
│       ├── axios.js                            // 封装的http请求方法
│       ├── directives.js                       // vue全局公用指令
│       ├── filters.js                          // vue全局公用过滤器
│       └── mixin.js                            // 公用混合工具类
│   ├── App.vue                                 // 页面入口文件
│   ├── main.js                                 // 程序入口文件，加载各种公共组件
│   └── static                                  // 静态资源文件夹
├── favicon.ico                                 // 图标
├── index.html                                  // 入口html文件
└── package.json                                // .
```

# 当前实现的功能
>>资讯类
- [x] 获取文章列表
- [x] 获取文章详情
- [x] 获取咨询分类列表
- [x] 获取咨询分类
- [x] 获取推荐信息
- [x] 获取首页全部咨询
>>用户类
- [x] 获取用户信息
- [x] 发送短信验证码
- [x] 注册账号
- [x] 修改用户信息
- [x] 修改/设置密码
- [x] 登录
- [x] 保存地址
- [x] 获取单个地址信息
- [x] 获取地址列表
- [x] 删除地址
- [x] 使用钱包支付订单
- [x] 收藏店铺
- [x] 获取我的收藏店铺
- [x] 添加、删除、修改收货地址
>>商城类
- [x] 获取商品目录信息
- [x] 获取商品列表
- [x] 获取商品详情    
- [x] 搜索商品
- [x] 加入购物车
- [x] 删除选购产品
- [x] 获取选购的产品信息
- [x] 确认选购产品，将作为下单的产品信息
- [x] 获取确认选购的产品信息
- [x] 创建订单 !
- [x] 确认收货
- [x] 取消订单
- [x] 获取订单列表
- [x] 获取订单详情
- [x] 获取店铺信息
- [x] 商品评论列表
- [x] 发布评论

## 相关使用技术链接

- [Vue](https://github.com/vuejs/vue)
- [mintUi](https://github.com/ElemeFE/mint-ui)
- [Vuex](https://github.com/vuejs/vuex)
- [webpack](https://github.com/webpack/webpack)




