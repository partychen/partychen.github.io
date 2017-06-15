### How to get a long period op token for api request.
Use chrome to go to the [swagger site]( https://op-build-prod.azurewebsites.net/swagger/ui/index#/), open the **"Authorization"** tab and the **"POST /v1/Authorizations/github/basicauth"** tab as below pitcure. There are 3 parameters should be filled.
![](https://pandao.github.io/editor.md/examples/images/4.jpg)
###### 1.X-OP-githubOtp: 
it's the github two-factor code, if you enable the github two-factor, you should fill this, or you can skip it.
###### 2. Authorization: 
this a basic auth token of your github account and github password, you can use some tool to generate it.
> the format should like "Basic Z2l0aHViX2FjY291bnQ6Z2l0aHViX3Bhc3N3b3Jk"
###### 3.X-OP-AADUserToken: 
this is the add token, it make sure you are a microsoft user and can pass the company AAD.
* Use chrome then go to the [portal](https://op-portal-prod.azurewebsites.net), login with github.(if you already login, please logout first.)
* After login the portal, click the **Secure** in the top left of browser, you can see it like below. then click the **cookie** link.![](https://pandao.github.io/editor.md/examples/images/4.jpg)
* Click to view the **X-OP-AADUserToken**, and copy it's content.
![](https://pandao.github.io/editor.md/examples/images/4.jpg)
After fill these parameters, click **"Try it out!"**, if success there will show no content, or you will get the error information. Then same as before, to click the **Secure** in the top left of browser and check the **cookie** with key of **"X-OP-BuildUserToken"**, then the value is the op token.
