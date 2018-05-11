FORMAT: 1A
HOST: http://vrapi.ledu.com

# VR项目game上报数据接口
本文档主要对 VR项目中游戏对后面请求接口数据进行描述.


# Group sendgamedata
		
## sendgamedata [/api/recivedata/gamedata]

### 上报数据日志接口 [POST]
例：gameid=1 的key为 zcvbnfgdfgertert4rfgfgdfgs 
加密字段：game_token,device_id,event_type,time 
加密方式:加密字段按首字母sort排序 sign=md5(device_id=832C1D16-4270-4887-845D-F91DD01403AA&event_type=1&game_token=25937484000257283130&time=1525918544&key) 
   
+ Parameters

    + game_token: `25937484000257283130` (string, optional) - 单次游戏的唯一token 
    + gameid: `1` (string, optional) - 注册的游戏编号（由服务端定义）            
    + device_id: `832C1D16-4270-4887-845D-F91DD01403AA` (string, optional)  - 设备号  
    + event_type: `1` (string, optional)  - 发送的数据事件类型 （注册）
    + data: `{}` (json, optional) - 具体上报数据
    + time: `1525918544` (string, optional)  - 时间戳（精确到s）
    + sign: `fdgfgdfgdfgdfgdfgfgfdgfdgfdgfdg` (string, optional)  - 加密字符串 
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "code": 0,
	          "msg":"success"
            }
			
			
# Group oparatedata
		
## oparatedata [/api/recivedata/oparatedata]

### 上报操作日志接口 [POST]
例：gameid=1 的key为 zcvbnfgdfgertert4rfgfgdfgs 
加密字段：game_token,device_id,event_type,time 
加密方式:加密字段按首字母sort排序 sign=md5(device_id=832C1D16-4270-4887-845D-F91DD01403AA&event_type=1&game_token=25937484000257283130&time=1525918544&key) 
   
+ Parameters
    + game_token: `25937484000257283130` (string, optional) - 单次游戏的唯一token 
    + gameid: `1` (string, optional) - 注册的游戏编号（由服务端定义） 
    + device_id: `832C1D16-4270-4887-845D-F91DD01403AA` (string, optional)  - 设备号  
    + event_type: `1` (string, optional)  - 发送的数据事件类型 1 游戏开始 2结束关卡 3 继续游戏 4退出游戏
    + data: `{}` (json, optional) - 具体上报数据
    + time: `1525918544` (string, optional)  - 时间戳（精确到s）
    + sign: `fdgfgdfgdfgdfgdfgfgfdgfdgfdgfdg` (string, optional)  - 加密字符串 
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "code": 0,
	          "msg":"success"
            }

# Group rule
		
## rule [/api/recivedata/rule]

### 游戏拉起进程前检测游戏是否合法接口 [GET]
例：gameid=1 的key为 zcvbnfgdfgertert4rfgfgdfgs 
加密字段：game_token,device_id,event_type,time 
加密方式:加密字段按首字母sort排序 sign=md5(device_id=832C1D16-4270-4887-845D-F91DD01403AA&event_type=1&game_token=25937484000257283130&time=1525918544&key) 
   
+ Parameters
    + game_token: `25937484000257283130` (string, optional) - 单次游戏的唯一token 
    + gameid: `1` (string, optional) - 注册的游戏编号（由服务端定义） 
    + device_id: `832C1D16-4270-4887-845D-F91DD01403AA` (string, optional)  - 设备号  
    + event_type: `1` (string, optional)  - 发送的数据事件类型 （是否可以拉起游戏）
    + time: `1525918544` (string, optional)  - 时间戳（精确到s）
    + sign: `fdgfgdfgdfgdfgdfgfgfdgfdgfdgfdg` (string, optional)  - 加密字符串 
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "code": 0,//0合法 1不合法
	          "msg":"success"
            }

			
## rule [/api/recivedata/iscancontinue]

### 继续游戏时请求后端是否可以继续接口 [GET]
例：gameid=1 的key为 zcvbnfgdfgertert4rfgfgdfgs 
加密字段：game_token,device_id,event_type,time 
加密方式:加密字段按首字母sort排序 sign=md5(device_id=832C1D16-4270-4887-845D-F91DD01403AA&event_type=1&game_token=25937484000257283130&time=1525918544&key) 
   
+ Parameters
    + game_token: `25937484000257283130` (string, optional) - 单次游戏的唯一token 
    + gameid: `1` (string, optional) - 注册的游戏编号（由服务端定义） 
    + device_id: `832C1D16-4270-4887-845D-F91DD01403AA` (string, optional)  - 设备号  
    + event_type: `1` (string, optional)  - 发送的数据事件类型 （是否可以拉起游戏）
    + time: `1525918544` (string, optional)  - 时间戳（精确到s）
    + sign: `fdgfgdfgdfgdfgdfgfgfdgfdgfdgfdg` (string, optional)  - 加密字符串 
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
	
    + Body

            {
              "code": 0,//0 可以继续 1余额不足 请支付
	          "msg":"success"
            }
	
