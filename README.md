# APU2

Mac address:
- black: 
    - wifi: 04F021457CA4
    - ethernet: fe80::20d:b9ff:fe4e:7784
- blue:  
    - wifi: 04F021457CA2
- red:   
    - wifi: 04F021457CA5



## Step 1: Install a linux distro on apu2 ( [Offical documentation](https://pcengines.ch/howto.htm#home) )

### Debian (work)

[Guida utilizzata](https://syscall.eu/blog/2017/07/19/apu/)

- Far partire la USB sulla apu
- Premere freccia giú finche non compare la scritta `Display help screens; type 'menu' at boot prompt to return to this menu" press "enter`
- Scrivere ¨menu¨ e premere invio
- premere F6
- dopo `boot: ` scrivere `install console=ttyS0,115200n8` e premere invio
- aspettare


### Ubuntu (work)

Must download [http://cdimage.ubuntu.com/releases/18.04.2/release/?_ga=2.6837746.1317156672.1557303868-755951356.1557213959](Ubuntu alternate)

Once at the "boot:" prompt type:

install vga=off console=ttyS0,115200n8

### Ubuntu server 18.04 LTS (not working)

Install the .iso on the USB with Unetbootin (iso mode).

Cambiando il file /boot/grub/boot.cfg e sostiuendo al post di `vga=...` -> ´console=ttyS0,115200n8´, in teoria si dovrebbe riuscire ma invece no. 

Il file boot.cfg c´é solo masterizzando la iso in ISO MODE. 

## Step 2: Preseeding

- Boot Ubuntu USB, but at the grub menu press F6 and choose ¨Expert Mode¨ 
- type: ´ksdevice=ens1 locale=en_US.UTF-8 keyboard-configuration/layoutcode=us hostname=ubuntu interface=ens1 url=http://

