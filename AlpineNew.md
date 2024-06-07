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

6. tambahkan disamping hostfwd
```BASH
,hostfwd=tcp::9000-:9000
```
jika ingin menambahkan ram tambahkan
```BASH
2048
```
setelah -m atau 1024 ganti menjadi 2048
hit ctrl + x hit enter

7.
```BASH
cat startqemu.sh
```

8.
```BASH
./startqemu.sh
```

9. Booting Linux Alpine

Note =>

username : root

password : Secret123

```BASH
docker --version
```
10.
```BASH
docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
```

11.
```BASH
docker ps
```

12. Buka browser
```BASH
http://localhost:9000
```

13. Jika ada kendala sukses web buka web dan gagal login
```BASH
sudo docker restart portainer to restart Portainer
```
