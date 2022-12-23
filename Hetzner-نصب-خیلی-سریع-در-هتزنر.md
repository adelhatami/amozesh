
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
مطابق عکس IP خود را کپی کنید و در مرورگر باز کنید

![image](https://user-images.githubusercontent.com/114227601/206861323-1de41700-6ce4-403a-a644-0836e2a22876.png)


یادتون نره حداقل 10 دقیقه  صبر کنیدا


اینجا باید دامنه خود را وارد کنید. توجه کنید که این لینک را در جایی  کپی کنید وگرنه بعد از یک ساعت دیگر قابل دسترسی نیست.

![image](https://user-images.githubusercontent.com/114227601/209338222-f877bdb5-41eb-4a9b-bbf7-3dff453679a8.png)

تبریک!

سرور پروکسی شما آماده است. 
![صفحه راهنمای کاربران](https://user-images.githubusercontent.com/114227601/206908372-db1fc206-4c6a-4206-ad39-e6b6b44a55c4.png)
