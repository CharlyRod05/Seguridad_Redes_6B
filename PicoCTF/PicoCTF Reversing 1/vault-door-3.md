### vault-door-3
### Descripcion
This vault uses for-loops and byte arrays.The source code for this vault is here: [VaultDoor3.java](https://challenge-files.picoctf.net/c_fickle_tempest/efe249b50ae104ab4d1c33f14838fda6b584138e36739834ac7cb4cb29f5b2d2/VaultDoor3.java)
### Solucion
Codigo fuente: 
```
import java.util.*;

class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
        String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
        if (vaultDoor.checkPassword(input)) {
            System.out.println("Access granted.");
        } else {
            System.out.println("Access denied!");
        }
    }

    // Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        System.out.println(s); //Añadido
        return s.equals("jU5t_a_sna_3lpm15g64e_u_4_m1r74d");
    }
}
```
el system.out final se añade para que al ingresar el password que viene en el propio codigo nos imprima el password correcto porque lo desordena en los mismos lugares

```
┌──(kali㉿kali)-[~/reversing/vaultdoors/3vaultdoor]
└─$ java VaultDoor3       
Enter vault password: PicoCTF{jU5t_a_sna_3lpm15g64e_u_4_m1r74d}
jU5t_a_s1mpl3_an4gr4m_4_u_e1675d
Access denied!
                                                                             
┌──(kali㉿kali)-[~/reversing/vaultdoors/3vaultdoor]
└─$ java VaultDoor3
Enter vault password: PicoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_e1675d}
jU5t_a_sna_3lpm15g64e_u_4_m1r74d
Access granted.
```


PicoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_e1675d}
### Notas adicionales

### Referencias
