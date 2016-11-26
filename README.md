# chage_key_map_win

Confirmed to work on windows 7 64bit.
Create a reg file and execute as an administrator.


Caps2Ctrl.reg (CRLF, SJIS)
Windows Registry Editor Version 5.00
[HKEY_LOCAL_MACHINE\SYSTEM/CurrentControlSet\Control\Keyboard Layout]
"Scancode Map" hex:00,00,00,00,00,00,00,00,03,00,00,00,1d,00,3a,00,3a,00,1d,00,00,00,00,00


Caps2Esc.reg (CRLF, SJIS)
Windows Registry Editor Version 5.00
[HKEY_LOCAL_MACHINE\SYSTEM/CurrentControlSet\Control\Keyboard Layout]
"Scancode Map" hex:00,00,00,00,00,00,00,00,03,00,00,00,01,00,3a,00,3a,00,01,00,00,00,00,00


Reference (in Japanese) --Thanks!
http://www.saluteweb.net/~oss_keyswap.html
