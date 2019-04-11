# Exercícios Aula 4 página 3
```shell
sudo ifconfig enp2s0 10.4.0.225 netmask 255.255.0.0 up
``` 

De forma permanente:
```shell
sudo nano /etc/network/interfaces
```

Adicionar no ficheiro:
```interfaces
iface enp2s0 inet static
	address 10.4.0.226/24
```


# Exercícios Aula 4 página 11
1. Editar o ficheiro hostname:
    ```shell
    sudo nano /etc/hostname
    ```

    Mudar o nome que está no ficheiro para GSRx.isctem.com

2. Editar o ficheiro resolv.conf:
    ```shell
    sudo nano /etc/resolv.conf
    ```

    Substituir o nameserver actual para:
    ```resolv.conf
    nameserver 10.4.0.250
    ```

# Exercícios Aula 4 página 17

1. TODO

2. Editar o ficheiro /etc/rsyslog.d/50-default.conf:
    ```shell
    sudo nano /etc/rsyslog.d/50-default.conf
    ```
    
    Adicionar a linha:
    ```
    mail.*			/var/log/logscorreio
    ```
    
    Máquina Vizinha:
    ```
    mail.*			@<IP_DA_MÁQUINA_VIZINHA>
    ```
