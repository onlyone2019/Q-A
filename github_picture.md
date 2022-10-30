# github图片显示不出来

比如这样：
![](https://github.com/onlyone2019/Q-A/blob/master/pictures/github_picture.png)

**原因：**
DNS污染

**解决方案：(windows)**
将下面这部分加入 `C:\Windows\System32\drivers\etc\hosts`
```python
140.82.113.3      github.com
140.82.114.20     gist.github.com
151.101.184.133    assets-cdn.github.com
151.101.184.133    raw.githubusercontent.com
151.101.184.133    gist.githubusercontent.com
151.101.184.133    cloud.githubusercontent.com
151.101.184.133    camo.githubusercontent.com
151.101.184.133    avatars0.githubusercontent.com
199.232.68.133     avatars0.githubusercontent.com
199.232.28.133     avatars1.githubusercontent.com
151.101.184.133    avatars1.githubusercontent.com
151.101.184.133    avatars2.githubusercontent.com
199.232.28.133     avatars2.githubusercontent.com
151.101.184.133    avatars3.githubusercontent.com
199.232.68.133     avatars3.githubusercontent.com
151.101.184.133    avatars4.githubusercontent.com
199.232.68.133     avatars4.githubusercontent.com
151.101.184.133    avatars5.githubusercontent.com
199.232.68.133     avatars5.githubusercontent.com
151.101.184.133    avatars6.githubusercontent.com
199.232.68.133     avatars6.githubusercontent.com
151.101.184.133    avatars7.githubusercontent.com
199.232.68.133     avatars7.githubusercontent.com
151.101.184.133    avatars8.githubusercontent.com
199.232.68.133     avatars8.githubusercontent.com
185.199.111.133    raw.githubusercontent.com 
185.199.110.133    raw.githubusercontent.com 
185.199.108.133    raw.githubusercontent.com 
185.199.109.133    raw.githubusercontent.com
```

不放心的话还可以执行一下下面这条命令：
```python
ipconfig /flushdns   # 刷新DNS记录 
ipconfig /renew      # 重新从DHCP服务器获得IP
```