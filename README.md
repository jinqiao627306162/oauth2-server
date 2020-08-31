客户端模式
1) http://localhost:9401/oauth/authorize?response_type=code&client_id=admin&redirect_uri=http://www.baidu.com&scope=all&state=normal
   response:https://www.baidu.com/?code=08HrBn&state=normal
2) postman
   authorization: username:admin 
                  password:admin123456
   body:grant_type            authorization_code
       code                   08HrBn
       client_id              admin
       redirect_uri           http://www.baidu.com
       scope                  all
       
       
       
     response:{
              "access_token": "cdf98716-06ab-45da-a637-339d014f0462",
              "token_type": "bearer",
              "expires_in": 3599,
              "scope": "all"
            }
3) http://localhost:9401/user/getCurrentUser?access_token=cdf98716-06ab-45da-a637-339d014f0462    

密码模式
http://localhost:9401/oauth/token

authorization: username:admin 
                  password:admin123456
                  
body:grant_type            password
       username              admin
       password           123456
       scope                  all
       

response:{
        "access_token": "cdf98716-06ab-45da-a637-339d014f0462",
        "token_type": "bearer",
        "expires_in": 3065,
        "scope": "all"
      }
