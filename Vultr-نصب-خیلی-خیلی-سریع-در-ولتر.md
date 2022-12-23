<div dir="rtl" markdown="1">


ابتدا کد زیر را کپی کنید

<div dir="ltr" markdown="1">

```
#cloud-config
package_upgrade: true
packages:
  - apt-transport-https
  - ca-certificates
  - curl
  - wget
  - gnupg-agent
  - software-properties-common
  - git

runcmd:
  - cd /opt
  - git clone https://github.com/hiddify/hiddify-config/
  - cd hiddify-config
 # uncomment it for using a special secret other wise it will be createed automatically
 # - echo "USER_SECRET=0123456789abcdef0123456789abcdef" >config.env
 # - echo "MAIN_DOMAIN=" >>config.env
  - echo "TELEGRAM_AD_TAG=" >>config.env
  - bash install.sh

final_message: "The system is finally up, after $UPTIME seconds"
output: { all: "| tee -a /root/cloud-init-output.log" }

# you can see the generated link from the website by using http://yourip/ or https://yourip.sslip.io in one hour, after that, it will be disapear. 
```
</div>

سپس در قسمت سرور تیک زیر را فشار دهید و کد بالا را در آن قرار دهید

![image](https://user-images.githubusercontent.com/114227601/206862792-ed30c212-efe4-47cf-8973-c3129a09499f.png)

پس از حداکثر 10 تا 15 دقیقه سرور شما آماده و پروکسی فعال خواهد بود


حالا باید دامنه را تنظیم کنیم. بر روی [این لینک](https://github.com/hiddify/hiddify-config/wiki/%D8%B1%D8%A7%D9%87%D9%86%D9%85%D8%A7%DB%8C-%D8%AA%D9%86%D8%B8%DB%8C%D9%85-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D9%87%D8%A7%DB%8C%DB%8C-%DA%A9%D8%B1%D8%AF%D9%86-%D9%86%D8%B5%D8%A8) کلیک کنید تا نصب را نهایی کنید .
</div>

