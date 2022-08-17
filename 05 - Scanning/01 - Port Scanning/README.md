# Port Scanning

# The `search portscan` Command

- Metasploit has a number of modules to scan open ports on the target system and network. You can list potential port scanning modules available using the `search portscan` command. 
  
  ![Screenshot (858)](https://user-images.githubusercontent.com/63872951/185216251-936df0bf-e0f1-4d3a-b113-f20ad4574bbe.png)

- Port scanning modules will require you to set a few options:
  
  
    - **CONCURRENCY:** Number of targets to be scanned simultaneously.
    
    - **PORTS:** Port range to be scanned. Please note that `1-1000` here will not be the same as using Nmap with the default configuration. Nmap will scan the `1000` most used                    ports, while Metasploit will scan port numbers from `1 to 10000`.
    
    - **RHOSTS:** Target or target network to be scanned.
    
    - **THREADS:** Number of threads that will be used simultaneously. More threads will result in faster scans.

  ![Screenshot (860)](https://user-images.githubusercontent.com/63872951/185216828-25b60fd0-1243-4934-b86f-dc840aedbbad.png)

- You can directly perform Nmap scans from the msfconsole prompt as shown below faster:

  ![Screenshot (861)](https://user-images.githubusercontent.com/63872951/185217089-6825c7ed-5029-4f1d-aea8-bd2576084af7.png)

- As for information gathering, if your engagement requires a speedier approach to port scanning, Metasploit may not be your first choice. However, a number of modules make Metasploit a useful tool for the scanning phase.
