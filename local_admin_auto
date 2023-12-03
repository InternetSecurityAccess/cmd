pushd "%~dp0"
chcp 65001
@echo on
SETLOCAL EnableExtensions

echo ADMIN creating ....
echo. >> AMDIN.txt
echo HOSTNAME >> ADMIN.txt
echo. >> AMDIN.txt
hostname >> ADMIN.txt
echo. >> AMDIN.txt
echo. >> ADMIN.txt
echo IP ADDRESS >> ADMIN.txt
ipconfig | findstr v4 >> ADMIN.txt
ipconfig | findstr v6 >> ADMIN.txt
echo. >> ADMIN.txt
set usernameset=admin%random%
call set usernameadmin=%usernameset%
echo LOGIN AND PASSWORD ADMINSTRATOR!!! >> ADMIN.txt
echo. >> ADMIN.txt
timeout 5 /nobreak
net user %usernameadmin% /add /random >> ADMIN.txt
echo. >> ADMIN.txt
chcp 1251
net localgroup "Администраторы" %usernameadmin% /add & if errorlevel 1 (net localgroup Administrators %random%l /add)
chcp 65001
goto end

:end
endlocal
popd
exit
