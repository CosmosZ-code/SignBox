# SignBox签到盒

```
     _______. __    _______ .__   __. .______     ______   ___   ___ 
    /       ||  |  /  _____||  \ |  | |   _  \   /  __  \  \  \ /  / 
   |   (----`|  | |  |  __  |   \|  | |  |_)  | |  |  |  |  \  V  /  
    \   \    |  | |  | |_ | |  . `  | |   _  <  |  |  |  |   >   <   
.----)   |   |  | |  |__| | |  |\   | |  |_)  | |  `--'  |  /  .  \  
|_______/    |__|  \______| |__| \__| |______/   \______/  /__/ \__\                                                                     
```

为你自动签到各个平台。

|   平台   |            名称             |        签到内容        | cookie时长 | 状态 |
| :------: | :-------------------------: | :--------------------: | :--------: | :--: |
|  米游社  | GenShinSign原神社区自动签到 |     米游社原神签到     |    未知    |  🟢️   |
| bilibili |      BiLiBiLi自动签到       | bilibili签到和每日任务 |    未知    |  🟢️   |



## 特性

- [x] 支持【青龙面板】/【crontab】多种定时方式
- [x] **支持多账号** 不同账号的`Cookie`值之间以列表分隔，如：`['cookie1','cookie2']`

## 使用方法

配置完成后定时运行main.py

【青龙面板】

点击添加任务

![image-20211211162229545](C:\Users\42796\AppData\Roaming\Typora\typora-user-images\image-20211211162229545.png)

【crontab】

输入`crontab -e`

添加一行 `0 7 * * * /bin/python3 /root/SignBox/main.py`

![image-20211211162626626](C:\Users\42796\AppData\Roaming\Typora\typora-user-images\image-20211211162626626.png)

## GenShinSign原神社区自动签到

**可以自动化为你获取原神每日福利。**

**使用步骤：**

​	1.1**获取cookie**

```js
var cookie = document.cookie;
var ask = confirm('Cookie:' + cookie + '\n\n是否复制内容到剪切板？');
if (ask == true) {
    copy(cookie);
    msg = cookie;
} else {
    msg = 'Cancel';
}
```

- 按`F12`，打开`开发者工具`，找到`Console`并点击

- 命令行粘贴代码并运行，获得类似`Cookie:xxxxxx`的输出信息

- `xxxxxx`部分即为所需复制的`Cookie`，点击确定复制到粘贴板

  1.2**配置congfig.py**

  ![image-20211211154048214](C:\Users\42796\AppData\Roaming\Typora\typora-user-images\image-20211211154048214.png)

- 将粘贴板复制到genshinCookies里面，`xxxx`部分即为所需复制的`值`。

### BiLiBiLi自动签到

**可以自动化为你签到b站并且完成每日任务。一起早日到6级吧！**

**使用步骤：**

1.1**获取cookie**

![image-20211211160434179](C:\Users\42796\AppData\Roaming\Typora\typora-user-images\image-20211211160434179.png)

- 按`F12`，打开`开发者工具`，找到Application并点击
- 再点击Cookie和https://www.bilibili.com/
- 把bili_jct和SESSDATA的值复制config.py中的biliCookies内
- `xxxx`部分即为所需复制的`值`，请对应复制进去
- ![image-20211211161015767](C:\Users\42796\AppData\Roaming\Typora\typora-user-images\image-20211211161015767.png)

