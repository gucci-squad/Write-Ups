# HTB-invite
Registering for HTB

## Getting an Invite Code for HTB
* unminify or run <script defer src="/js/inviteapi.min.js"> found on the /invite webpage
  * You'll get:
 ```
 function verifyInviteCode(code){var formData={"code":code};$.ajax({type:"POST",dataType:"json",data:formData,url:'/api/invite/verify',success:function(response){console.log(response)},error:function(response){console.log(response)}})}function makeInviteCode(){$.ajax({type:"POST",dataType:"json",url:'/api/invite/how/to/generate',success:function(response){console.log(response)},error:function(response){console.log(response)}})}
 ```
* POST /api/invite/how/to/generate 
  * You'll get:
  * S1FQWEktUlFYQ0otS05aSkItUkhMU08tWkRGRFE= 
  * `In order to generate the invite code, make a POST request to /api/invite/generate`
* POST /api/invite/generate 
  * You'll get:
  * `base64 invite code`
