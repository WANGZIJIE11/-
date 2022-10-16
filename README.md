不要私自用我的源码进行非法盈利
此代码只分享给我的粉丝
里面有我的私人key
看到此条信息，希望是从小羊会修电脑的过来的
如不是会被限制使用
基于Github Actions实现每天固定运行一次 需注意GithubActions使用的UTC时间 转换为北京时间需要+8小时处理
小羊建议如果时间无法运行或者运行几天后报错，更改一下时间。

`master分支github actions执行规则是每天早上7点自动执行`
`如果需要监听推送执行 请切换workflow_on_push分支`
 
 
#### 公众号模板内容 可以根据自己的需要变更内容
```text
你的名字{{friendName.DATA}}
今年{{howOld.DATA}}
距离下一次生日{{nextBirthday.DATA}}天
具体我们的下一次纪念日{{nextMemorialDay.DATA}}天
现在在{{province.DATA}}{{city.DATA}}
当前天气{{weather.DATA}}
当前气温{{temperature.DATA}}
风力描述{{winddirection.DATA}}
风力级别{{windpower.DATA}}
空气湿度{{windpower.DATA}}
{{author.DATA}}
{{origin.DATA}}
{{content.DATA}}
```
其中
```text
{{author.DATA}}
{{origin.DATA}}
{{content.DATA}}
```
是古诗的变量，如果`Bootstrap`中配置未开启随机古诗 那么这三个就是不要的


#### 核心类介绍

```
Application.java          // 启动类
Bootstrap.java            // 一些启动配置(公众号信息在这里配置)
core/MessageFactory.java  // 创建微信消息对象的代码就在这里面 有需要可以自己修改下变量
```
