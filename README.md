# awesome-doskey
Awesome doskey commands will go here.

    cat=type $* 
    alias=doskey $* & doskey /macros > c:\ProgramData\doskey\macros.doskey & echo done
    savedoskey=doskey /macros > c:\ProgramData\doskey\macros.doskey & echo done & echo -------------------- & type c:\ProgramData\doskey\macros.doskey
    showdoskey=type c:\ProgramData\doskey\macros.doskey
    lss=dir /D/O:GN | findstr /i $*
    gtdoskey=cd c:\ProgramData\doskey
    ls=dir /D/O:GN $* 
    doskeys=type c:\ProgramData\doskey\macros.doskey | findstr /i $*
    calc=explorer.exe shell:appsFolder\Microsoft.WindowsCalculator_8wekyb3d8bbwe!App 
    apt=choco $* 
    openf=explorer . 
    clipf=type $* | clip 
    touch=fsutil file createnew $1 0 
    watch30=for /l %g in () do @( $* ^& timeout /t 30 )
    myip=ipconfig | findstr IPv4
    clipf=type $* | clip
    myipl=curl ifconfig.ovh
    touch=fsutil file createnew $1 0
    np=notepad++ $*
    ip=ipconfig | findstr IPv4
    cp=xcopy $1 $2 /s /e
    edithosts=notepad++ c:\Windows\System32\drivers\etc\hosts
    ss=netstat -ano
    ssp=netstat -ano | findstr /i $*
    ps=tasklist
    psid=tasklist /fi "pid eq $*"

# How to have persistent doskeys?
    ==> reg add "HKCU\Software\Microsoft\Command Processor" /v Autorun /d "doskey /macrofile=\"d:\bat\macros.doskey\"" /f
    The operation completed successfully.

    ==> reg query "HKCU\Software\Microsoft\Command Processor" /v Autorun

    HKEY_CURRENT_USER\Software\Microsoft\Command Processor
        Autorun    REG_SZ    doskey /macrofile="d:\bat\macros.doskey"
