#### 简单介绍     
本项目为cf2dns宝塔插件版。     
为了方便部署，因此将原项目github.com/ddgth/cf2dns做成了宝塔插件。      
功能上主要用于将CloudFlare CloudFront Gcore优选IP地址解析到您的域名记录中。     
   
#### 云服务监测平台(https://monitor.gacjie.cn)     
由于近期移动抽风屏蔽eu.org域名，影响监测脚本提交数据，故我把域名全换掉了。     
不再使用eu.org域名，请大家及时更换新的地址链接。    
    
#### 演示图片    
 ![cf2dns.jpg](https://raw.githubusercontent.com/gacjie/cf2dns/main/cf2dns.jpg)   
         
#### 功能说明    
支持从GacJieMonitor(monitor.gacjie.cn)获取CloudFlare、CloudFront、Gcore优选IP地址   
支持从HostMonit(stock.hostmonit.com)获取CloudFlare优选IP地址          
支持将优选IP解析至DNSPOD        
支持将优选IP解析至阿里云解析          
支持将优选IP解析至华为云解析          
支持查询授权余额          
支持ipv4&ipv6同时获取并解析                 
         
#### 价格计费（GacJieMonitor）    
插件免费提供授权码o1zrmHAF，可永久免费使用。    
付费KEY购买请加Q群699927761联系群主，以获得独享优选IP。     
插件按照接口获取次数计费，暂时定价为3块钱3000次，10块钱12000次。   
按照每15分钟获取一次，一个月需要消耗2880次左右。   
接口每次请求会缓存数据15分钟，请求缓存数据不会计费。     
如果同时开启IPV4&IPV6选项，将会消耗双倍积分。
           
#### 注意事项    
插件安装时请关闭宝塔系统加固插件，会终止安装脚本的执行。     
插件只会更新电信、移动、联通三网线路的IP，因此还需要将回退源设置到默认线路上。    
使用插件前请确保您的网站域名使用cname或saas方式接入，并且域名解析在dnspod、华为云、阿里云的国内版。
          
#### 使用说明   
将本项目ZIP包下载到电脑，打开面板-软件商店-第三方应用-导入安装即可    
        
#### 2024年01月16日更新记录          
增加用户添加空主机名直连留空的错误判断，并输出错误提示。     
增加添加域名的配置项提示，以避免看不懂配置项名称的情况。     
增加前端显示判断，以显示已经选定的配置项。      
       
#### 常见问题        
      
Q：为什么不支持海外dns解析运营商？     
A：由于cf等cdn属于泛播，移动联通电信需要单独解析，才能实现三网优选。海外dns均不支持国内三网线路解析。      
如不方便使用国内云解析 可以访问 https://monitor.gacjie.cn/page/cname/index.html 获取公共cname地址使用。       
     
Q：使用该插件更新IP后，导致网站全都打不开了？      
A：使用优选IP的前提是，cdn使用cname(别名)方式接入，本插件只是将获取的优选IP解析到您的域名上去，网站打不开是因为你的CDN配置问题。        
     
Q：该插件安全吗？      
A：插件是基于cf2dns增加了宝塔可视化操作界面。并且代码全部公开在github上面，可先自行审查代码再决定是否安装。      
      
Q：为什么不做成其他面板的插件？      
A：由于cf2dns源代码是基于python3编写的，而宝塔面板的运行环境也是python3，所以可以很方便的写成插件，不需要考虑python3环境问题。       