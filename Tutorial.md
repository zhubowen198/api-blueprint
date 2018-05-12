FORMAT: 1A
HOST: http://vrapi.ledu.com

# VR项目game数据接口的data json定义
本文档主要对 VR项目中游戏对后端请求接口数据data进行描述.


# Group sendgamedata
上报日志包括（1.注册日志 2.登录日志 3.玩家行为日志 4.游戏异常）	
## sendgamedata 

### 一：上报数据日志接口---注册日志data
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
			  "gameuniqureid":1,//游戏中的唯一id
			  "vrplatid":"oQThqweSPYlUt8R3f7iji3AEz8G8" //vr平台传递的唯一标识
			  "registertime“:1525918544,//注册时间
			
## sendgamedata 

### 二：上报数据日志接口---登录日志 data
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
			  "gameuniqureid":1,//游戏中的唯一id
			  "vrplatid":"oQThqweSPYlUt8R3f7iji3AEz8G8" //vr平台传递的唯一标识
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
              "gameuniqureid":1,//游戏中的唯一id
			  "vrplatid":"oQThqweSPYlUt8R3f7iji3AEz8G8" //vr平台传递的唯一标识
			  "oparate_type”：1,//1 游戏开始 2.加载结束 3结束关卡 4 继续游戏 5退出游戏
			  "checkpoint"：1,//当前关卡
			  "create_time":1525918544,//操作时间

            }
			
## sendgamedata 

### 四：上报数据日志接口--设备异常 data
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

             {
			  "gameuniqureid":1,//游戏中的唯一id
			  "vrplatid":"oQThqweSPYlUt8R3f7iji3AEz8G8" //vr平台传递的唯一标识
			  "errorcode"：1,//错误码
			  "error_msg":"头盔异常",//异常提示
            }
			
			
			
# Group oparatedata
上报操作日志包括（1 游戏开始 2.加载结束 3结束关卡 4 继续游戏 5退出游戏）
		
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

### 上报操作日志--加载结束
   
+ Parameters
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "checkpoint"：1,//当前关卡
	          "create_time":1525918544,//加载结束时间
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


