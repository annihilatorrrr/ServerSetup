# ServerSetup
My server setup script!.

to use a webhook use:

must have a domain in cloudflare; take from freemnom then transfer it to there
> after that go to tunnels & make a tunnel for free and setup it in the server ( follow the on screen steps. )
> take the url use paste it in url of webhook of bot.
> now do screen then set port for ex. 443 which has been provided in the local host url of cloudflare tunnel; then ```sudo su``` then activate virtual env then cd and run it.
> must do ```git config --global --add safe.directory /home/ubuntu/folder``` for git pull support and ```sudo chown -R ubuntu /home/ubuntu/venv/```


## Open port in orcale:
```
sudo apt install firewalld
sudo firewall-cmd --zone=public --permanent --add-port=443/tcp
sudo firewall-cmd --reload
sudo iptables -I INPUT -m state --state NEW -p tcp --dport 443 -j ACCEPT
sudo netfilter-persistent save
```
then open in the protal!
