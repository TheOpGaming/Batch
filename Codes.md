
# Codes - Batch :
  Codes that were converted into .exe programs to show they are not malicious.


# Codes - Troll Scripts :
  These will not be here as you can copy the code by going to http://www.github.com/TheOpGaming/VBS


# Code Menu (Updating) 1.3
  Code:
  @echo off
@color f

IF NOT EXIST "C:\Program Files (x86)\Google\Chrome\Application" (
 start http://www.google.com/chrome
)
IF EXIST "C:\Program Files (x86)\Google\Chrome\Application" (
 start chrome http://www.google.com/chrome
)




set Version=Alpha 1.3

















set computername=%random%







If NOT exist ".\Var" (
 @md Var
) 
 
ping localhost -n 2 >nul

if NOT exist ".\Var\StartTitle.data" (
 echo %computername% > .\Var\StartTitle.data
)


@title %computername%



If NOT exist ".\Var\UserID.txt" (
 echo %random% > .\Var\UserID.txt
) 









if EXIST ".\Var\UserID.txt" (
for /f "Delims=" %%a in (.\Var\UserID.txt) do (

set UserID=%%a

)
  )



if NOT exist ".\Var\PCNAME.data" (
 set /p cpuname=New Script Name: 
)

@title %cpuname% - Menu (%version%) by TheOpGaming.


if NOT exist ".\Var\PCNAME.data" (
 echo %cpuname% > .\Var\PCNAME.data
)






if EXIST ".\Var\PCNAME.txt" (
for /f "Delims=" %%a in (.\Var\PCNAME.data) do (

set cpuname=%%a

)
  )

  
if EXIST ".\Var" (
 echo %cpuname% - Menu (%version%)> .\Var\MenuTitle.data
)

ping localhost -n 2 >nul

if EXIST ".\Var\PCNAME.data" (
for /f "Delims=" %%a in (.\Var\MenuTitle.data) do (

set title=%%a

)
  )

  
  
  
  
  


if EXIST ".\Var\PCNAME.data" (
for /f "Delims=" %%a in (.\Var\PCNAME.data) do (

set cpuname=%%a

)
  )

@attrib +s +h .\Var

@attrib +s +h .\Var\UserID.txt

If NOT exist ".\Var\Pass.txt" (
 echo 123 > .\Var\Pass.txt
) 
if NOT EXIST ".\Var\Inactive.ini" (
 echo false > .\Var\Inactive.ini
)



if EXIST ".\Var\Pass.txt" (
for /f "Delims=" %%a in (.\Var\Pass.txt) do (

set LPass=%%a

)
  )


if %lpass%==123 goto CPASS
if %lpass%==12 goto CPASS


for /f "Delims=" %%a in (.\Var\Inactive.ini) do (

set Inactive=%%a

)

if %Inactive%==true goto reactivate
if %Inactive%==false echo Menu is not inactive.

goto start1

:start
@attrib +s +h .\Var
ping localhost -n 5 >nul
cls
color f


for /f "Delims=" %%a in (.\Var\Inactive.ini) do (

set Inactive=%%a

)

if %Inactive%==true goto reactivate
if %Inactive%==false echo Menu is not inactive.
echo.
echo Version %version%
echo.
@title %cpuname% - Menu (%version%) by TheOpGaming.
ping localhost -n 3 >nul
:start1
if not exist ".\Version" (
 md .\Version
)
echo %version%>.\Version\Version.data
attrib +s +h .\Version
attrib +s +h +r .\Version\Version.data
cls
color f
echo.
echo Version %version%
echo.
echo.
echo UserID: %userid%
echo.
echo Select:
echo.
echo Create (Change your password)
echo.
echo Close
echo.
echo Login
echo.
echo ChangeID (Change your UserID)
echo.
echo Reinstall
echo.
set /p Choice=Choose From The Above Options: 
echo.
echo Please wait...
ping localhost -n 3 >nul

if %choice%==create goto create
if %choice%==close goto close
if %choice%==login goto login
if %choice%==Create goto create
if %choice%==Close goto close
if %choice%==Login goto login
if %choice%==ChangeID goto uuidc
if %choice%==changeid goto uuidc
if %choice%==Roblox goto roblox
if %choice%==roblox goto roblox
cls
color c
echo Invalid Choice: %choice%      
ping localhost -n 3 >nul
goto start



:create
color f
title Option: Create
cls
for /f "Delims=" %%a in (.\Var\Pass.txt) do (

set Text=%%a

)
if %text%==123 goto CPASS
set /p LPass=Current Password: 
if %LPass%==%Text% goto CPASS
echo.
color c
echo Incorrect!
ping localhost -n 3 >nul
goto start






:CPASS
cls
echo.
set /p Pass=Enter Your New Password: 
cls
ping localhost -n 3 >nul
if %Pass%==123 goto PassFail
if %Pass%==12 goto PassFail
if %Pass%==1 goto PassFail
if %Pass%==0 goto PassFail
echo %Pass% > ".\Var\Pass.txt"
echo.
color a
if EXIST ".\Var\Pass.txt" (
  echo Password Changed!
)

echo [%TIME%] (%DATE%) Password Changed! >> .\Var\Log.txt
ping localhost -n 5 >nul
goto start






:close
title Option: Close
cls
ping localhost -n 2 >nul
cls
echo.
exit






:login
cls
title Option: Login
echo.
set /p eid= Enter your UserID: 
for /f "Delims=" %%a in (.\Var\UserID.txt) do (

set UserID=%%a

)

if %eid%==%UserID% goto uidlog
echo Invalid User ID!
echo [%TIME%] (%DATE%) Login Failure! (UserID Attempted: %userid%) >> .\Var\Log.txt
ping localhost -n 3 >nul
goto start






:uidlog
ECHO.
set /p LPass= Password: 
for /f "Delims=" %%a in (.\Var\pass.txt) do (

set Text=%%a

)

if %LPass%==%Text% goto yes
color c
title Login Failure!
echo Incorrect Password!
echo [%TIME%] (%DATE%) Login Failure! (Password Attempted: %LPass%) >> .\Var\Log.txt
echo [%TIME%] (%DATE%) Login Failure! (UserID Attempted: %userid%) >> .\Var\Log.txt
ping localhost -n 5 >nul
goto start




:yes
cls
title Login Success!
color a
echo Login Success!
echo [%TIME%] (%DATE%) Login Success! >> .\Var\Log.txt
echo.
ping localhost -n 5 >nul
color f
title [Logged In] Menu (%verrsion%)
:logged


cls
echo.
echo Select folder to open (CaSe SeNsEtIvE):
echo.
echo C
echo.
echo PC
echo.
echo AppData
echo.
echo Var (The file used for this menu)
echo.
echo More
echo.
ping localhost -n 3 >nul
set /p open=Folder to open: 
if %open%==appdata start %userprofile%\AppData
if %open%==c start C:\
if %open%==var start .\Var
if %open%==PC start explorer.exe
if %open%==pc start explorer.exe
if %open%==Appdata start %userprofile%\AppData
if %open%==AppData start %userprofile%\AppData
if %open%==C start C:\
if %open%==Var start .\Var
if %open%==More goto moreoptions
if %open%==more goto moreoptions


echo Opening %open%...
ping localhost -n 3 >nul
goto logged












:uuidc
cls
title Option: Change UserID!
cls
echo.
set /p eid1= Enter your UserID: 
for /f "Delims=" %%a in (.\Var\UserID.txt) do (

set UserID=%%a

)
if %eid1%==%UserID% goto uuidchange
echo Invalid User ID!
echo [%TIME%] (%DATE%) UserID Change Failure! (UserID Attempted: %userid%) >> .\Var\Log.txt
ping localhost -n 3 >nul
goto start











:uuidchange
cls
set /p newid=Set your NEW UserID: 



for /f "Delims=" %%a in (.\Var\UserID.txt) do (

set UserID=%%a

)
attrib -s -h -r .\Var\UserID.txt
:numbers.......
if %newid%==0 goto cnope
if %newid%==01 goto cnope
if %newid%==001 goto cnope
if %newid%==0001 goto cnope
if %newid%==1 goto cnope
if %newid%==2 goto cnope
if %newid%==3 goto cnope
if %newid%==4 goto cnope
if %newid%==5 goto cnope
if %newid%==6 goto cnope
if %newid%==7 goto cnope
if %newid%==8 goto cnope
if %newid%==9 goto cnope
:letters........
if %newid%==a goto error2.1
if %newid%==b goto error2.1
if %newid%==c goto error2.1
if %newid%==d goto error2.1
if %newid%==e goto error2.1
if %newid%==f goto error2.1
if %newid%==g goto error2.1
if %newid%==h goto error2.1
if %newid%==i goto error2.1
if %newid%==j goto error2.1
if %newid%==k goto error2.1
if %newid%==l goto error2.1
if %newid%==m goto error2.1
if %newid%==n goto error2.1
if %newid%==o goto error2.1
if %newid%==p goto error2.1
if %newid%==q goto error2.1
if %newid%==r goto error2.1
if %newid%==s goto error2.1
if %newid%==t goto error2.1
if %newid%==u goto error2.1
if %newid%==v goto error2.1
if %newid%==w goto error2.1
if %newid%==x goto error2.1
if %newid%==y goto error2.1
if %newid%==z goto error2.1
if %newid%==A goto error2.1
if %newid%==B goto error2.1
if %newid%==C goto error2.1
if %newid%==D goto error2.1
if %newid%==E goto error2.1
if %newid%==F goto error2.1
if %newid%==G goto error2.1
if %newid%==H goto error2.1
if %newid%==I goto error2.1
if %newid%==J goto error2.1
if %newid%==K goto error2.1
if %newid%==L goto error2.1
if %newid%==M goto error2.1
if %newid%==N goto error2.1
if %newid%==O goto error2.1
if %newid%==P goto error2.1
if %newid%==Q goto error2.1
if %newid%==R goto error2.1
if %newid%==S goto error2.1
if %newid%==T goto error2.1
if %newid%==U goto error2.1
if %newid%==V goto error2.1
if %newid%==W goto error2.1
if %newid%==X goto error2.1
if %newid%==Y goto error2.1
if %newid%==Z goto error2.1

echo %newid% > .\Var\UserID.txt
ping localhost -n 3 >nul
cls

for /f "Delims=" %%a in (.\Var\UserID.txt) do (

set UserID=%%a

)


if %newid%==%userid% echo UserID has been changed.
if NOT %newid%==%userid% echo UserID could not be changed.
if NOT %newid%==%userid% set errorlevel=1
if %errorlevel%==1 goto error1
ping localhost -n 5 >nul
attrib +s +h .\Var\UserID.txt
goto start









:cnope


for /f "Delims=" %%a in (.\Var\UserID.txt) do (

set UserID=%%a

)


if NOT %newid%==%userid% echo UserID could not be changed.
set errorlevel==2

if %errorlevel%==1 goto error1
if %errorlevel%==2 goto error2
ping localhost -n 5 >nul
exit

:error2
title Error Level: 2
echo UserID cannot be 1 Number
ping localhost -n 5 >nul
goto start




:error2.1
title Error Level: 2
echo UserID cannot be 1 Letter
ping localhost -n 5 >nul
goto start





:error1
title Error 1: Access denied.
cls
echo.
echo Access is denied to edit your UserID
ping localhost -n 5 >nul



















:moreoptions

cls
echo.
echo Select what to do (CaSe SeNsEtIvE):
echo.
echo Close (%cpuname%%title%)
echo.
echo Start (Goto the start of the menu and Logout)
echo.
echo Clear (Clear the screen, Sets the menu to Inactive.)
echo.
echo Back
echo.
ping localhost -n 3 >nul
set /p open=Select: 

if %open%==Close exit
if %open%==close exit
if %open%==Clear goto cls
if %open%==clear goto cls
if %open%==back goto logged
if %open%==Back goto logged
if %open%==Start goto start
if %open%==start goto start




















:cls
cls
echo.
echo true > .\Var\Inactive.txt
:cls1
cls
echo.
echo The Menu is Inactive...
ping localhost -n 10 >nul
exit






:reactivate
cls
color f
title Reactivating...
echo The menu is currently Inactive, Reactivation has been started...


ECHO.
set /p LPass= Password: 
for /f "Delims=" %%a in (.\Var\Pass.txt) do (

set Text=%%a

)

if %LPass%==%Text% goto reactivate1
color c
title Reactivation Failure!
echo.
echo Incorrect Password %LPass%!
echo.
echo You failed to reactivate the menu!
ping localhost -n 5 >nul
goto reactivate




:reactivate1
cls
color f
echo false > .\Var\Inactive.ini
echo.
@color a
echo You activated the menu!
ping localhost -n 5 >nul
goto start
exit






:PassFail
title Failed...
cls
echo %pass% is not valid... Use A Different Password
ping localhost -n 5 >nul
goto cpass


#End of MENU



#  Code (Secret File Coming Soon):
    The file has not yet been uploaded... The code will be here when it is...


