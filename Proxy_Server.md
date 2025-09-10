Proxy server 
All request in Linux comes through this proxy server (privacy control security and performance)

dnf install squid -y ((^C))
vim /etc/squid/squid.conf 
acl my_localnet src ip/mask
Scroll down to mind http access comment em and next line http access <name>

Leave a line or two after the last line then,
request_header_access Referer deny all
request _header_access X-Forwarded-For deny all
request_header_acess Via deny all
request_header_access Cache-Control deny all
Come out
systemctl enable --now squid
firewall-cmd --add-service=squid --permanent
firewall-cmd --reload
vim/etc/profile.d/proxy.sh (to make all req go through proxy) (enter it) (port:3428)
Go in 
(Creating a variable) MY_PROXY_URL=" prox.codiculture.net:3128"(eg)
HTTP_PROXY=$MY_PROXY_URL
HTTPS_PROXY=$MY_PROXY_URL
FTP_PROXY=$MY_PROXY_URL
Export the above proxy like HTTP_PROXY HTTPS_PROXY
Create seperate for cap letters and smaller ones too
COME OUT
source /etc/profile.d/proxy.sh( to apply the changes)