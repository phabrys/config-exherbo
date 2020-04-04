  GNU nano 4.9.1                                          README.md                                           Modifié  
# config-exherbo

## Installation d'Ehxerbo

Etapes d'installation d'Exherbo

1. mount /dev/exherbo/root /mnt/exherbo
2. cd /mnt/exherbo
3. wget https://dev.exherbo.org/stages/exherbo-x86_64-pc-linux-gnu-current.tar.xz
4. wget	https://dev.exherbo.org/stages/sha1sum
5. grep exherbo-x86_64-pc-linux-gnu-current.tar.xz sha1sum | sha1sum -c
6. tar xJpf exherbo-x86_64-pc-linux-gnu-current.tar.xz
7. vim /etc/fstab
4. mount -o rbind /dev /mnt/exherbo/dev
5. mount -o rbind /sys /mnt/exherbo/sys
6. mount -t proc none /mnt/exherbo/proc
5. mount /dev/nvme0n1p4	/mnt/exherbo/boot
6. mount /dev/nvme0n1p1	/mnt/exherbo/boot/efi
7. cp /etc/resolv.conf /mnt/exherbo/etc/resolv.conf
5. chroot /mnt/exherbo /bin/bash
6. source /etc/profile
7. export PS1="(exherbo) $PS1"
8. git clone https://github.com/phabrys/config-exherbo.git

