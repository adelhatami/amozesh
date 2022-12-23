
![image](https://user-images.githubusercontent.com/114227601/206861285-58832cec-a2a3-441e-91d4-8300d16584d6.png)

حالا کد زیر را کپی کنید
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
کد بالا را در محل نشان داده در عکس قرار دهید.
![image](https://user-images.githubusercontent.com/114227601/206861304-656682b4-17a3-44c1-89f9-7b0d89566728.png)

پس از حداکثر 10 تا 15 دقیقه سرور شما آماده و پروکسی فعال خواهد بود
مطابق عکس آی پی خود را کپی کنید و در مرورگر باز کنید

![image](https://user-images.githubusercontent.com/114227601/206861323-1de41700-6ce4-403a-a644-0836e2a22876.png)


یادتون نره حداقل 10 دقیقه  صبر کنیدا

حالا باید دامنه را تنظیم کنیم. بر روی [این لینک](https://github.com/hiddify/hiddify-config/wiki/%D8%B1%D8%A7%D9%87%D9%86%D9%85%D8%A7%DB%8C-%D8%AA%D9%86%D8%B8%DB%8C%D9%85-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D9%87%D8%A7%DB%8C%DB%8C-%DA%A9%D8%B1%D8%AF%D9%86-%D9%86%D8%B5%D8%A8)کلیک کنید تا نصب را نهایی کنید .