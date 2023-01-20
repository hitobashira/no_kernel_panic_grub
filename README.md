# no_kernel_panic manjaro_bootable
Easyway. Make manjaroLinux,antergos,archLinux bootable.

## 2023 JAN. 21 
tested kernel on Manjaro.
- initrd /boot/amd-ucode.img /boot/initramfs-6.1-x86_64.img
- initrd /boot/amd-ucode.img /boot/initramfs-6.0-x86_64.img
- initrd /boot/amd-ucode.img /boot/initramfs-5.15-x86_64.img


Kernel　Panic :: Figure 0
![kernelpanic](https://github.com/hitobashira/no_kernel_panic/blob/master/kernelpanic.png)

## manjaro_bootable.pl Ver.0.8.1 alpha test. 2018-03-25,09-13,9-20
 make bootable (ubuntu/Mint)grub.cfg ,manjaro/archlinux entry.
```
 Only Run command on ubuntu/Mint.
``` 

![UEFI SSD](https://github.com/hitobashira/no_kernel_panic/blob/master/Screenshot.png)

# Why this program is necessary
## for multiboot users (eg. ubuntu and archlinux and the other , linuxmint and manjaro and windows10)
ubuntu and its derivative Linux Mint bring in a kernel panic of antergos, archlinux, etc. with 100% probability every time of Kernel configuration.

I think that this phenomenon occurred several years ago. Strangely, no one will cure it even if there is a report. Probably we only need to fix os-prober that update-grub calls, but sh is hard for me.

So I wrote a workaround in Perl. In my environment, it works properly.

If it does not go well
```
$ sudo update-grub
```
Please issue. However, it can only be returned to grub.cfg where the original manjaro does not start (boot).
```
/tmp/grub.cfg backup
```
Danger!! Run command with ROOT/Superuser privileges. 
```
type in terminal on Ubuntu/LinuxMint.

$ sudo /fullpath/manjaro_bootable.pl -V 

cf.
$ sudo     ~/bin/manjaro_bootable.pl -V 

```
## (bonus) It is a script to check if manjaro is bootable. on ubuntu/mint's grub.
```
$ sudo GrubChk #on ubuntu/mint without manjaro.

```


Example of operation :: Figure 1
![fig01.png](https://github.com/hitobashira/no_kernel_panic/blob/master/fig01.png)

Example of operation :: Figure 2
![fig02.png](https://github.com/hitobashira/no_kernel_panic/blob/master/fig02.png)

 
### Better Practice!! You may install your bootloader at manjaro partation.
And shall be given Happy, a little.
 
### author
https://poor-user.blogspot.com/

I have been testing for about half a year. 
I think that there is no fatal bug already, so I will try to make it public. It will be useful for about 3 people worldwide.

# License

This programs is GPL. you have to read GPL.txt.
