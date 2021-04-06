# rkm

Проверить процессор на аппаратную виртуализацию

egrep -c '(vmx|svm)' /proc/cpuinfo 
cat /proc/cpuinfo | grep -E  '(vmx|svm)' 

Установить пакеты kvm // ubuntu
sudo apt install qemu qemu-kvm libvirt-daemon libvirt-clients bridge-utils virt-manager ovmf

Установить пакеты kvm // debian
apt-get install qemu-kvm libvirt-clients libvirt-daemon-system

Добавить пользователя kvm

sudo gpasswd -a $USER libvirt

Проверить работу сервиса
sudo systemctl status libvirtd

virsh войти в управление виртуальной машины
net-list --all
net- tab-tab
net-info default
exit
ip a посмотреть все сетевые адаптеры
sudo iptables -vnL
net-start default запуск сети
net-edit default
net-autostart default (название сети)
sudo iptables -vnL -t nat
net-destroy 
