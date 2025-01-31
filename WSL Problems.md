# Internet access issues

wsl cannot access internet / resolve names

    sudo nano /etc/resolv.conf 
    
put # before existing entries, add nameserver 8.8.8.8 on its own line, save (Ctrl+X; Y; Enter), ping google.com to make sure it worked, then to make sure it doesn't get overwritten: 
    
    sudo nano /etc/wsl.conf 
    
add [network] on its own line, then generateResolvConf = false on the next line, save, and you're done. 

