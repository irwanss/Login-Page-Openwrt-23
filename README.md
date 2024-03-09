1. Install unzip<br>
opkg update && opkg install unzip

2. Download login page<br>
cd
wget https://github.com/irwanss/Login-Page-Openwrt-23/raw/master/loginpage.zip
unzip loginpage.zip

3. Backup login page bawaan<br>
cd /usr/share/ucode/luci/template/
mv sysauth.ut sysauthbc.ut 

4. Install login page<br>
cd /root/loginpage/
mv sysauth.ut /usr/share/ucode/luci/template/sysauth.ut
mv loginpage.css /www/luci-static/material/
mv bg.jpeg /www/luci-static/material/
cd
rm -rf loginpage loginpage.zip

------------------------------------------------------------------------------------------------------

1. Kembalikan login page bawaan<br>
cd /usr/share/ucode/luci/template/
rm -rf sysauth.ut
mv sysauthbc.ut sysauth.ut
rm -rf /www/luci-static/material/loginpage.css /www/luci-static/material/bg.jpeg
