# Payloads Module

- Payloads are codes that will run on the target system.

- Exploits will leverage a vulnerability on the target system, but to achieve the desired result, we will need a payload. 
- Examples could be; getting a shell, loading a malware or backdoor to the target system, running a command, or launching calc.exe as a proof of concept to add to the penetration test report. 
- Starting the calculator on the target system remotely by launching the `calc.exe` application is a benign way to show that we can run commands on the target system.

- Running command on the target system is already an important step but having an interactive connection that allows you to type commands that will be executed on the target system is better. 
- Such an interactive command line is called a `shell`. Metasploit offers the ability to send different payloads that can open shells on the target system. 

  ![Screenshot (838)](https://user-images.githubusercontent.com/63872951/184820058-0d7496d1-4a32-426d-8685-83b76db72b2d.png)
