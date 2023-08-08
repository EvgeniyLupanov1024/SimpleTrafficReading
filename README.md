<img alt="work_in_progress" align="middle" width="30%" src="https://raw.githubusercontent.com/LupanovEvgeniyHTML/LupanovEvgeniyHTML/main/img/work_in_progress.jpg"/> 

## Зависимости

- DPDK

Установка и конфигурация:
```
sudo apt-get update ;\
sudo apt-get install -y python libpcap-dev build-essential meson ninja;\
sudo apt-get install -y linux-headers-`uname -r` ;\
;\
wget http://git.dpdk.org/dpdk/snapshot/dpdk-23.07.tar.xz ;\
tar xvf dpdk-23.07.tar.xz ;\
cd dpdk-23.07/ ;\
;\
meson build ;\
cd build ;\
ninja ;\
ninja install ;\
ldconfig ;\
```
