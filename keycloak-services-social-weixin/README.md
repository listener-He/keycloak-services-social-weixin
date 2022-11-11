# keycloak-services-social-weixin

To install the social weixin one has to:（English VERSION）

* Add the jar to the Keycloak server:
  * `$ cp target/keycloak-services-social-weixin-*.jar _KEYCLOAK_HOME_/providers/

* Add tow templates to the Keycloak server:
  * `$ cp templates/realm-identity-provider-weixin.html _KEYCLOAK_HOME_/themes/base/admin/resources/partials`
  * `$ cp templates/realm-identity-provider-weixin-ext.html _KEYCLOAK_HOME_/themes/base/admin/resources/partials`


# 使用说明(中文)
1. 安装
```
    cp keycloak-services-social-weixin-0.0.2.jar  _KEYCLOAK_HOME_/providers/
    cp templates/realm-identity-provider-weixin.html _KEYCLOAK_HOME_/themes/base/admin/resources/partials
    cp templates/realm-identity-provider-weixin-ext.html _KEYCLOAK_HOME_/themes/base/admin/resources/partials
``` 

2. 重启keycloak （后台运行）
启动前自行杀死进程
```
    cd _KEYCLOAK_HOME_/bin/
    ./kc.sh start-dev &
```


# 版本更新
    * v1.0_20221110  

1 增加自适应微信登录功能。

2 账号关联默认使用微信unionid，如unionid不存在则使用openId

3 pc和wechat使用同一套账号则必须绑定同一个开放平台，否则会绑定不同账号

4 wechat信息非必填,默认使用pc方式登录

5 _KEYCLOAK_HOME_/themes/base/admin/resources/partials 文件夹不存在，可通过mkdir -p 手动创建

6 redirectURL 跳转地址需要手动修改，具体参考源码



