# chage_key_map_win

Confirmed to work on 64bit windows 7 and 10.
Create a reg file and execute as an administrator.


switchCapsAndCtrl.reg (CRLF, SJIS)
Windows Registry Editor Version 5.00
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout]
"Scancode Map"=hex:00,00,00,00,00,00,00,00,03,00,00,00,1d,00,3a,00,3a,00,1d,00,00,00,00,00


switchCapsAndEsc.reg (CRLF, SJIS)
Windows Registry Editor Version 5.00
[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout]
"Scancode Map"=hex:00,00,00,00,00,00,00,00,03,00,00,00,01,00,3a,00,3a,00,01,00,00,00,00,00


!CAUTION: WINDOWS IS ENDIAN!

00 00 00 00 ; version
00 00 00 00 ; flag
05 00 00 00 ; the number of instructions
1d 00 3a 00 ; the key function of left 2 bytes are mapped to the key of right 2 bytes（work as left Ctrl ← Caps）
3a 00 1d 00 ; the key function of left 2 bytes are mapped to the key of right 2 bytes（work as Caps ← left Ctrl）
01 00 29 00 ; the key function of left 2 bytes are mapped to the key of right 2 bytes（work as ESC ← half/ful width）
29 00 01 00 ; the key function of left 2 bytes are mapped to the key of right 2 bytes(work as half/full width ← ESC）
00 00 00 00 ; termination

key codes are following
left Ctrl：        00 1d
CapsLock：         00 3a
ESC：              00 01
half/full width：  00 29


Reference (in Japanese) --Thanks!
http://www.saluteweb.net/~oss_keyswap.html
