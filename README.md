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
```
в конец файла meson_options.txt добавить строку
```
option('enable-avx2', type: 'boolean', value: false, description:
    'compile with AVX2 support')
```

```
meson build ;\
cd build ;\
ninja install ;\
sudo ldconfig ;\
```
