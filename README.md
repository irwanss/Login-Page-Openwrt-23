1. Install unzip<br>
opkg update && opkg install unzip

2. Download login page<br>
cd<br>
wget https://github.com/irwanss/Login-Page-Openwrt-23/raw/master/loginpage.zip<br>
unzip loginpage.zip<br>

3. Backup login page bawaan<br>
cd /usr/share/ucode/luci/template/<br>
mv sysauth.ut sysauthbc.ut <br>

4. Install login page<br>
cd /root/loginpage/<br>
mv sysauth.ut /usr/share/ucode/luci/template/sysauth.ut<br>
mv loginpage.css /www/luci-static/material/<br>
mv bg.jpeg /www/luci-static/material/<br>
cd<br>
rm -rf loginpage loginpage.zip<br>

------------------------------------------------------------------------------------------------------

1. Kembalikan login page bawaan<br>
cd /usr/share/ucode/luci/template/<br>
rm -rf sysauth.ut<br>
mv sysauthbc.ut sysauth.ut<br>
rm -rf /www/luci-static/material/loginpage.css /www/luci-static/material/bg.jpeg<br>
