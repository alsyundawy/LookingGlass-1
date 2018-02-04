# LookingGlass


## Install (centos 6.9 x64)

`git clone https://github.com/max2max/LookingGlass`<br />
`cd LookingGlass/LookingGlass`<br />
`bash configure.sh`<br />

Follow the instructions

`wget https://raw.githubusercontent.com/max2max/self/master/besttrace -O /usr/local/bin/besttrace`<br />
`chmod +x /usr/local/bin/besttrace`<br />
`echo "www ALL=(root)  NOPASSWD:/usr/local/bin/besttrace" >> /etc/sudoers`<br />
`echo "www ALL=(root)  NOPASSWD:/usr/sbin/hping3" >> /etc/sudoers`<br />
`service php-fpm restart`<br />

## License

Code is licensed under MIT Public License.

* If you wish to support my efforts, keep the "Powered by LookingGlass" link intact.
