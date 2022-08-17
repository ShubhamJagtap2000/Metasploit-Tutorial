# Working With Modules

# Step 1: Regular Command Prompt
```
Command : msfconsole
```
# Step 2: msfconsole Prompt
```
msf5> or msf6>
```
# Step 3: Decide to Use a Module

  ![Screenshot (842)](https://user-images.githubusercontent.com/63872951/184950846-fcbffb23-3975-459d-be70-b113c8ca4c5b.png)

# Step 4: A Context Prompt

- Once you have decided to use a module and used the set command to chose it, the msfconsole will show the context. You can use context-specific commands (e.g. ***set RHOSTS 10.10.x.x***) here.

# Step 5: The meterpreter Prompt

  ![Screenshot (850)](https://user-images.githubusercontent.com/63872951/185065304-c2406f99-5b67-4302-b224-01f62cb77cdb.png)

# Step 6: show options Command

- The show options command will list all available parameters.
  
  ![Screenshot (844)](https://user-images.githubusercontent.com/63872951/184951014-a5c1bc74-66c4-4238-b3ac-9f027fa5af39.png)

# Step 7: set RHOSTS, RPORT, LHOSTS, PAYLOAD, SESSION, etc

## Parameters that you will often use in this step

**1. RHOSTS:** ***Remote host***, the ***IP address*** of the ***target*** system. A single IP address or a network range can be set. This will support the `CIDR (Classless Inter-Domain Routing)` notation (/24, /16, etc.) or a network range `(10.10.10.x – 10.10.10.y)`. You can also use a ***file*** where targets are listed, one target per line using `file:/path/of/the/target_file.txt` <br>


**2. RPORT:** ***Remote port***, the port on the target system the vulnerable application is running on. <br>

**3. PAYLOAD:** The payload you will use with the exploit. <br>

**4. LHOST:** ***Localhost***, the ***attacking machine IP*** address. <br>

**5. LPORT:** ***Local port***, the port you will use for the reverse shell to connect back to. This is a port on your ***attacking*** machine, and you can set it to any port not used by any other application. <br>

**6. SESSION:** Each connection established to the target system using Metasploit will have a ***session ID***. You will use this with post-exploitation modules that will connect to the target system using an existing connection. <br>

### **<ins>Once you have set a parameter, you can use the `show options` command to check the value was set correctly.</ins>**
<br>

# Other Steps

## Shell on the Target Sysytem

- Once the ***exploit is completed***, you may have access to a command shell on the target system. This is a regular command line, and all commands typed here run on the target system.
```
C:\Windows\system32>
```

## The unset all Command

- You can also clear any parameter value using the `unset` command or clear all set parameters with the `unset all` command.

  ![Screenshot (852)](https://user-images.githubusercontent.com/63872951/185169258-70cc3875-d5e7-492d-ab9a-b71a5ad7d4ca.png)

## The setg and unsetg Command

- You can use the `setg` command to set values that will be used for all modules. The setg command is used like the set command. 

- The ***difference*** is that if you use the set command to set a value using a module and you switch to another module, you will need to set the value again. The setg command allows you to set the value so it can be used by ***default*** across different modules. 

- You can ***clear*** any value set with setg using `unsetg`.

- The example below uses the following flow;

    - We use the ***ms17_010_eternalblue*** exploitable
    - We set the ***RHOSTS*** variable using the `setg` command instead of the `set` command
    - We use the `back` command to leave the exploit context
    - We use an **auxiliary** (this module is a scanner to discover ***MS17-010*** vulnerabilities)
    - The `show options` command shows the ***RHOSTS*** parameter is already populated with the **IP** address of the ***target*** system.
    
     ![Screenshot (853)](https://user-images.githubusercontent.com/63872951/185171752-1d48de7e-d300-4ea7-a5bc-731e5af3bc6e.png)

    
- The `setg` command sets a **<ins>global</ins>** value that will be used until you exit Metasploit or clear it using the `unsetg` command.

# Next Steps: 

## [Using Modules](https://github.com/ShubhamJagtap2000/Metasploit/tree/main/04%20-%20Working%20With%20Modules/Modules%20Usage)

## [Sessions](https://github.com/ShubhamJagtap2000/Metasploit/tree/main/04%20-%20Working%20With%20Modules/Sessions)
