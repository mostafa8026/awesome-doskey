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
