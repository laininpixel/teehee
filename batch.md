Various batch scripts I saved from an old job

chkdsk
```
@echo off echo ychkdsk [target drive, i.e. D] fr rem sleep 3600 rem cutilsshutdown.exe l r y t6
```

change ip address
```
Echo ipconfig/flushdns ipconfig/flushdns echo ipconfig/release ipconfig/release echo ipconfig/renew ipconfig/renew exit
```

sfc
```
sfc /scannow PAUSE Dism /Online /Cleanup-Image /RestoreHealth PAUSE 

sfc /scannow PAUSE

@ sfc /scannow @ pause
```

Delete temp
```
SET SRC1=C:\\Users SET SRC2=AppData\\Local\\Microsoft\\Windows\\Temporary Internet Files SET SRC3=AppData\\Local\\History SET SRC4=AppData\\Local\\Temp
FOR /D %%X IN ("%SRC1%\\*") DO FOR /D %%Y IN ("%%X\\%SRC2%\\*.*") DO RMDIR /S /Q "%%Y" FOR /D %%X IN ("%SRC1%\\*") DO FOR /D %%Y IN ("%%X\\%SRC3%\\*.*") DO RMDIR /S /Q "%%Y" FOR /D %%X IN ("%SRC1%\\*") DO FOR /D %%Y IN ("%%X\\%SRC4%\\*.*") DO RMDIR /S /Q "%%Y" FOR /D %%X IN ("%SRC1%\\*") DO FOR %%Y IN ("%%X\\%SRC3%\\*.*") DO DEL /F /S /Q "%%Y" FOR /D %%X IN ("%SRC1%\\*") DO FOR %%Y IN ("%%X\\%SRC4%\\*.*") DO DEL /F /S /Q "%%Y"

c:
cd\\Users\\%username%\\AppData\\Local\\Microsoft\\Windows\\Temporary Internet Files

del *.* /f /s /q

cd\\users\\%username%\\appdata\\local\\temp

del *.* /f /s /q

cd\\windows\\temp

del *.* /f /s /q

exit
