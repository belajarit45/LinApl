1.
```BASH
bash -c "$(curl -fsSL https://raw.githubusercontent.com/egandro/docker-qemu-arm/master/termux-setup.sh)"
```
2.
```BASH
ls
```
3.
```BASH
cd alpine
```
4.
```BASH
ls
```
5.
```BASH
nano startqemu.sh
```
6.
```BASH
cd ~/alpine/ && ./startqemu.sh
```
7. tambahkan disamping hostfwd
```BASH
,hostfwd=tcp::9000-:9000
```
hit ctrl + x hit enter
8.
```BASH
cat startqemu.sh
```
9.
```BASH
./startqemu.sh
```
Note =>
username : root
password : Secret123

10.
```BASH
docker --version
```
11.
```BASH
docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
```
12.
```BASH
docker ps
```
13. Buka browser
```BASH
http://localhost:9000
```

14. Jika ada kendala sukses web buka web dan gagal login
```BASH
sudo docker restart portainer to restart Portainer
```
