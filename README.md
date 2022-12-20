# Tutorial Testnet MINIMA

- [Website](https://minima.global/)
- [Discord](https://discord.gg/minima)
- [Doc offcial](https://docs.minima.global/)
- [Dashbord Node](https://incentive.minima.global/account/register?inviteCode=FICPALDD) 



# Buat akun dan dapatkan Incentive ID
- [Incentive Minima Global](https://incentive.minima.global/account/register?inviteCode=FICPALDD)
- Buka URL di atas 
- Buat akun isi informasi anda
- Email, Password, kode reff **FICPALDD**
- Verifikasi Email 
- Login dan Copy Incentive ID 
- Simpan dan Lanjut Step berikut

Jika menggunakan Android, PC, atau VPS silahkan ikuti tutorial masing-masing

## User Android

- Install Aplikasi Minima di [Play Store](https://play.google.com/store/apps/details?id=com.minima.android&hl=en&gl=US&pli=1)
- Buka Aplikasi
- Masuk dibagian **Incentive Program**
- Incentive ID
- Isi dengan Kode ID anda
- Done


### Terminal apps 
di home page Buka apps **Terminal** masukan command
```
incentivecash
```

[![uid.png](https://i.postimg.cc/h4d2PMnp/uid.png)](https://postimg.cc/mhTYmYtH)


## USER linux VPS 

### Step Add user minima
ini bisa di skip atau bisa menggunakan user root lanjut dibagian **Install Docker**

- buat password untuk user minima masukan nama bebas detail user tidak usah di isi tekan **enter** sampai konfirmasi **y**
```
sudo adduser minima
```
memberikan izin admin ke user **minima**
```
sudo usermod -aG sudo minima
```
login sebagai user minima
```
su - minima
```

### Install Docker
```
sudo curl -fsSL https://get.docker.com/ -o get-docker.sh
```
```
sudo chmod +x ./get-docker.sh && ./get-docker.sh
```
add user minima ke docker (skip jika menggunakan user root)
```
sudo usermod -aG docker $USER
```
```
exit
```
### RUN Node
login sebagai user minima
```
su - minima
```

```
docker run -d -e minima_mdspassword=123 -e minima_server=true -v ~/minimadocker9001:/home/minima/data -p 9001-9004:9001-9004 --restart unless-stopped --name minima9001 minimaglobal/minima:latest
```
di bagian `123` = ganti dengan password anda (saran huruf kecil + nomor saja)

### Start Docker
```
sudo systemctl enable docker.service
```
```
sudo systemctl enable containerd.service
```
Check docker yang sedang berjalan
```
docker ps
```
### MiniDapp hub setup ID
- Jika semua sudah normal lanjutkan setup ID
- edit dan buka di browser https://YourServerIP:9003/
di bagian `YourServerIP` ganti dengan IP VPS anda
- Masuk dibagian **Incentive Program**
- Incentive ID
- Isi dengan Kode ID anda
- Done
### Noted
- Jika Web Your **Connection is Not Private**
-  yang menggunakan crome Klik **Advanced**
-  Klik **Proceed to 1.1.1.1.0 (unsafe)**
[![uid.png](https://i.postimg.cc/0NjMn80Z/uid.png)](https://postimg.cc/cKqL4Gj8)




### Command Update otomatis (jika ada update terbaru)
```
docker run -d --restart unless-stopped --name watchtower -e WATCHTOWER_CLEANUP=true -e WATCHTOWER_TIMEOUT=60s -v /var/run/docker.sock:/var/run/docker.sock containrrr/watchtower
```

### Art-Team INFO
noted: **art team** here does not have any specific goals or intentions, they only collect data and share it with everyone.

untuk INFO Testnet lainya Silahkan join Discord 👇

[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/ArtSy5team)
[![Discord](https://img.shields.io/badge/discord-7289d9?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/EAKEdZU6c8)
[![Github](https://img.shields.io/badge/GitHub-171515?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/Art-Sy5team)
[![trakteer](https://img.shields.io/badge/trakteer.id-e31e1e?style=for-the-badge&logo=ko-fi&logoColor=white)](https://trakteer.id/Art-Sy5team/tip)
