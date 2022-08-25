# Example Workflow

#### 1. We will use the vulnerability scanning module that finds potential ***MS17-010 vulnerabilities*** with the use command:
```
auxiliary/scanner/smb/smb_ms17_010
```
#### 2. We set the RHOSTS value using `hosts -R`.
#### 3. We have typed `show options` to check if all values were assigned correctly. (In this example, ***10.10.138.32*** is the IP address we have scanned earlier using the `db_nmap` command)
#### 4. Once all parameters are set, we launch the exploit using the `run` or `exploit` command. 

  ![image](https://user-images.githubusercontent.com/63872951/186696448-e0decefb-3b0c-4845-bcaa-c13dd5245173.png)

  ![image](https://user-images.githubusercontent.com/63872951/186696607-3684c73f-42d4-4694-bb76-ba320061f3fd.png)

- If there is more than one host saved to the database, all IP addresses will be used when the `hosts -R` command is used. 

- In a typical penetration testing engagement, we could have the following scenario: 

    - Finding available hosts using the `db_nmap` command
    - Scanning these for further vulnerabilities or open ports (using a port scanning module) 

- The `services` command used with the `-S` parameter will allow you to search for specific services in the environment. 

  ![image](https://user-images.githubusercontent.com/63872951/186697066-e8c7e034-60e0-4c79-b91d-fd0d1f36dcf3.png)

- You may want to look for low-hanging fruits such as:

   - **HTTP:** Could potentially host a web application where you can find vulnerabilities like SQL injection or Remote Code Execution (RCE). 
   
   - **FTP:** Could allow anonymous login and provide access to interesting files. 
   
   - **SMB:** Could be vulnerable to SMB exploits like MS17-010
   
   - **SSH:** Could have default or easy to guess credentials
   
   - **RDP:** Could be vulnerable to Bluekeep or allow desktop access if weak credentials were used. 


- As you can see, Metasploit has many features to aid in engagements such as the ability to compartmentalize your engagements into workspaces, analyze your results at a high level, and quickly import and explore data.
