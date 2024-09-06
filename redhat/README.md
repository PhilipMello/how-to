# RedHat

### Recovery ROOT password
In the inicialization of the system press TAB and edit using "e".
insert "rd.break" in the end of the line (linux...... quiet rd.break), save with "CTRL+X".
wait the system boot up
check if /sysroot is "RO" using the command below:
```bash
mount
```
Change to "RW" with:
```bash
mount -o remount,rw /sysroot
```
Gain access to /sysroot with:
```bash
chroot /sysroot
```
you should gain access to bash now.
use command "passwd root" to change the root password of the root user.

DON'T EXIT YEAT.
create file with command: 
```bash
touch /.autorelabel
```
type "exit" twice to finish the process,
now the system will reboot.
congrats your password has been reset successfully.

