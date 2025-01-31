# To intgrate wsl with github
## Code to execute in wsl
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager-core.exe"

## more deatails
https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-git

# Git is teacking file permissions

to prevent git from tracking file permissions:

    git config core.filemode false

# Git should convert line ends to LF

## for linux: 

    git config core.autocrlf input

input ensures that Git converts CRLF to LF on commit but doesn't convert line endings on checkout. This is suitable for Unix-like systems (WSL2/Ubuntu).

## for windows: 
    
    git config core.autocrlf true

true ensures that Git converts CRLF to LF on commit and converts LF to CRLF on checkout. This is suitable for Windows.

