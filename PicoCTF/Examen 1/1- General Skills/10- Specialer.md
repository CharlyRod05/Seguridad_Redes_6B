# Reto
# Descripcion
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.`ssh -p 59796 ctf-player@saturn.picoctf.net`. The password is `483e80d4`
# Solucion

```
vladi@911:~/Desktop/retos/reto$ ssh -p 59796 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:59796 ([13.59.203.175]:59796)' can't be established.
ED25519 key fingerprint is: SHA256:lMXKIC17ONzyUJx7ZYBY5VSwoxCz20uq5/Nm+IhXKew
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:59796' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@saturn.picoctf.net's password: 
Specialer$ ls
-bash: ls: command not found
Specialer$ whoami 
-bash: whoami: command not found
Specialer$ cat
-bash: cat: command not found
Specialer$ 
!          bash       cd         declare    else       false      hash       let        pwd        shift      times      unalias    
./         bg         command    dirs       enable     fc         help       local      read       shopt      trap       unset      
:          bind       compgen    disown     esac       fg         history    logout     readarray  source     true       until      
[          break      complete   do         eval       fi         if         mapfile    readonly   suspend    type       wait       
[[         builtin    compopt    done       exec       for        in         popd       return     test       typeset    while      
]]         caller     continue   echo       exit       function   jobs       printf     select     then       ulimit     {          
alias      case       coproc     elif       export     getopts    kill       pushd      set        time       umask      }          
Specialer$ cd ../../           
bin/   home/  lib/   lib64/ 
Specialer$ cd ../../home
Specialer$ pwd
/home
Specialer$ ls            
-bash: ls: command not found
Specialer$ cd ctf-player/
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd ctf-player/
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd ctf-player/
Specialer$ cd   
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd ala/
Specialer$ echo $(<kazam.txt)
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_d5ef8b71}
```
### Flag: picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_d5ef8b71}

# Notas
Al entrar con ssh el entorno es restrictivo con los comandos basicos, tabee dos veces y me mostro un poco de informacion, probe moverme con cd y con el autocompletado me dio directorios, al navegar en el directorio de usuario hay carpetas como abra, ala o sim. Probe en las carpetas hasta en ala imprimi con echo el contenido de kazam.txt y me dio la bandera.
# Referencias
