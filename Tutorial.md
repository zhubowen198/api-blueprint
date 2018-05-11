FORMAT: 1A

# VR项目game数据接口的data json定义
本文档主要对 VR项目中游戏对后端请求接口数据data进行描述.


# Group sendgamedata
上报日志包括（1.注册日志 2.登录日志 3.玩家行为日志）	
## sendgamedata 

### 一：上报数据日志接口---注册日志data
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "gameid":1,//注册的游戏编号（由服务端定义）
			  "id":1,//用户的唯一标识id
			  "nick":"zhubowen",//昵称,
			  "union_id":"oQThqweSPYlUt8R3f7iji3AEz8G8" //微信的union_id
            }
			
## sendgamedata 

### 二：上报数据日志接口---登录日志 data
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
			  "id":1,//用户的唯一标识id
			  "nick":"zhubowen",//昵称,
			  "union_id":"oQThqweSPYlUt8R3f7iji3AEz8G8", //微信的union_id
			  "login_type":1, //1 登入 2登出
			  "create_time":1525918544,//操作时间
            }

## sendgamedata 

### 三：上报数据日志接口---玩家行为日志 data
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

             {
              "gameid":1,//注册的游戏编号（由服务端定义）
			  "id":1,//用户的唯一标识id
			  "nick":"zhubowen",//昵称,
			  "union_id":"oQThqweSPYlUt8R3f7iji3AEz8G8", //微信的union_id
			  "oparate_type”：1,//1 游戏开始 2结束关卡 3 继续游戏 4退出游戏
			  "checkpoint"：1,//当前关卡
			  "create_time":1525918544,//操作时间

            }
			
			
			
# Group oparatedata
上报操作日志包括（1 游戏开始 2结束关卡 3 继续游戏 4退出游戏）
		
## oparatedata 

### 上报操作日志--开始游戏
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "checkpoint"：1,//当前关卡
	          "create_time":1525918544,//开始时间
            }
			
			
## oparatedata 

### 上报操作日志--一继续游戏开始通知
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "checkpoint"：2,//当前关卡
	          "create_time":1525918550,//开始时间
            }
			
## oparatedata 

### 上报操作日志--一个场次的结束通知
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "checkpoint"：2,//当前关卡
	          "create_time":1525918550,//结束时间
            }

## oparatedata 

### 上报操作日志--一游戏结束退出通知
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "checkpoint"：2,//当前关卡
	          "create_time":1525918550,//退出时间
            }


