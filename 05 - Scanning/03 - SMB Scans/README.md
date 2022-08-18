# SMB Scans

- Metasploit offers several useful auxiliary modules that allow us to scan specific services. 
- Especially useful in a corporate network would be `smb_enumshares` and `smb_version` but please spend some time to identify scanners that the Metasploit version installed on your system offers. 

  ![Screenshot (866)](https://user-images.githubusercontent.com/63872951/185475057-d662d7b9-9b2c-451f-a678-ce564319c391.png)


- When performing service scans, it would be important not to omit more "exotic" services such as `NetBIOS`. 

- `NetBIOS`, ***Network Basic Input Output System***, similar to SMB, allows computers to communicate over the network to share files or send files to printers. 

- The NetBIOS name of the ***target*** system can give you an idea about its role and even importance (e.g. CORP-DC, DEVOPS, SALES, etc.). 

- You may also run across some shared files and folders that could be accessed either without a password or protected with a simple password (e.g. admin, administrator, root, toor, etc.).

- Remember, Metasploit has many modules that can help you have a better understanding of the target system and possibly help you find vulnerabilities. It is always worth performing a ***quick search*** to see if there are any modules that could be helpful based on your target system. 
