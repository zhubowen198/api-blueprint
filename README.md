FORMAT: 1A

# VR项目game上报数据接口
本文档主要对 VR项目中游戏对后面请求接口数据进行描述.

# Group sendgamedata
		
## sendgamedata [/api/device/regData]

### 上报数据日志接口 [POST]
   
+ Parameters
    + game_token: `25937484000257283130` (string, required) - 单次游戏的唯一token 
    + device_id: `832C1D16-4270-4887-845D-F91DD01403AA` (string, required)  - 设备号  
    + event_type: `1` (string, required)  - 发送的数据事件类型 （注册）
    + data: `` (json, required) - 具体上报数据
    + time: `1525918544` (string, required)  - 时间戳（精确到s）
    + sign: `fdgfgdfgdfgdfgdfgfgfdgfdgfdgfdg` (string, required)  - 加密字符串 
	
+ Request (application/json)
  
+ Response 200 (application/json)

    + Headers
    + Body

            {
              "code": 0,
	          "msg":"success"
            }

