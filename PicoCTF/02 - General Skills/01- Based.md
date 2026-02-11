### Based

### Descripcion
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

Additional details will be available after launching your challenge instance.

Connect with nc fickle-tempest.picoctf.net 55394.
### Solucion

```
CharlyRod-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 55394
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
^C
CharlyRod-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 55394
Let us see how data is stored
computer
Please give the 01100011 01101111 01101101 01110000 01110101 01110100 01100101 01110010 as a word.
...
you have 45 seconds.....

Input:
computer
Please give me the  o164 o141 o142 o154 o145 as a word.
Input:
table
Please give me the 74657374 as a word.
Input:
test
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_acdCcfCa}
```

Se resolvio con cyberchef
[From Binary - CyberChef](https://cyberchef.org/#recipe=From_Binary\('Space',8\)&input=MDExMDAxMTAgMDExMDAwMDEgMDExMDExMDAgMDExMDAwMTEgMDExMDExMTEgMDExMDExMTA)
[Find / Replace, From Octal - CyberChef](https://cyberchef.org/#recipe=Find_/_Replace\(%7B'option':'Regex','string':'o'%7D,'',true,false,true,false\)From_Octal\('Space'\)&input=bzE2NCBvMTQxIG8xNDIgbzE1NCBvMTQ1)
[From Charcode - CyberChef](https://cyberchef.org/#recipe=From_Charcode\('Space',16\)&input=NzQgNjUgNzMgNzQ)
### Notas adicionales
Para el ultimo es charcode de base 16
### Referencias
