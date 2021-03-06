#知乎关系网爬虫

![DEMO](https://github.com/starkwang/Spider/blob/master/demo.png?raw=true)

------
#使用方法
```
git clone https://github.com/starkwang/Spider.git && cd Spider

npm install

node index.js // Server runs at localhost:3000
```
------
#配置
`config.js`

- `cookie` [string]（必填项） : 自己在知乎上的cookie
- `\_xsrf` [string]（必填项）: 自己在知乎上的_xsrf
- `concurrency` [number]（可选项）: 请求的并发数，默认为3

**由于知乎的API较不稳定，concurrency并发数太大可能会造成卡死，在网络环境不好时建议设置为2或者1**

------

###附：cookie与_xsrf配置方法

打开知乎任意用户的关注者页，例如[https://www.zhihu.com/people/starkwei/followers](https://www.zhihu.com/people/starkwei/followers)

打开浏览器控制台，选择Network：
![DEMO](https://github.com/starkwang/Zhihu-Spider/blob/master/img/Snip20160323_1.png?raw=true)

下拉页面，会自动加载更多关注者，可以看到对`/node/ProfileFollowersListV2`这个接口发起了多次请求：
![DEMO](https://github.com/starkwang/Zhihu-Spider/blob/master/img/Snip20160323_2.png?raw=true)
打开请求详情，Cookie和_xsrf就在里面：
![DEMO](https://github.com/starkwang/Zhihu-Spider/blob/master/img/Snip20160323_3.png?raw=true)



