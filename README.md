# LookingGlass


## Install (centos 6.9 x64)
```bash
git clone https://github.com/max2max/LookingGlass
cd LookingGlass/LookingGlass
bash configure.sh
# follow the instructions of the shell
```
```bash
# download besttrace
if [ ! -f "/usr/local/bin/besttrace" ]; then
    wget https://github.com/max2max/self/raw/master/tools/besttrace -O /usr/local/bin/besttrace
    chmod +x /usr/local/bin/besttrace
fi

# grant privileges for php to execute besttrace
echo "www ALL=(root)  NOPASSWD:/usr/local/bin/besttrace" >> /etc/sudoers
echo "www ALL=(root)  NOPASSWD:/usr/sbin/hping3" >> /etc/sudoers
service php-fpm restart
```
## License

Code is licensed under MIT Public License.

* If you wish to support my efforts, keep the "Powered by LookingGlass" link intact.
