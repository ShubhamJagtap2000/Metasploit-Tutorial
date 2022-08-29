# How Meterpreter Works?

- Meterpreter is a Metasploit payload that supports the penetration testing process with many valuable components. 

- Meterpreter will run on the target system and act as an agent within a ***command and control*** architecture.

- Meterpreter runs on the target system but is ***not installed*** on it. 

- It runs in ***memory*** and does not write itself to the disk on the target. 

- This feature aims to avoid being detected during antivirus scans. 

- By default, most antivirus software will scan new files on the disk (e.g. when you download a file from the internet). Meterpreter runs in memory (`RAM` - Random Access Memory) to avoid having a file that has to be written to the disk on the target system (e.g. `meterpreter.exe`). 

- This way, Meterpreter will be seen as a process and not have a file on the target system. 

- Meterpreter also aims to avoid being detected by network-based `IPS` (***<ins>Intrusion Prevention System</ins>***) and `IDS` (***<ins>Intrusion Detection System</ins>***) solutions by using encrypted communication with the server where Metasploit runs (typically your ***attacking machine***). 

- If the target organization ***does not decrypt*** and inspect encrypted traffic (e.g. `HTTPS`) coming to and going out of the local network, `IPS` and `IDS` solutions will not be able to detect its activities.

- While Meterpreter ***is recognized*** by major antivirus software, this feature provides some degree of stealth.

- The example below shows a target Windows machine exploited using the `MS17-010` vulnerability. 

- You will see Meterpreter is running with a process ID, `PID of 1304`; this PID will be different in your case. 

- We have used the `getpid` command, which returns the process ID with which Meterpreter is running. 

- The process ID (or process identifier) is used by operating systems to identify running processes. 

- All processes running in Linux or Windows will have a `unique ID` number; this number is used to interact with the process when the need arises (e.g. if it needs to be stopped).

  ![image](https://user-images.githubusercontent.com/63872951/187141028-227c3ea6-1cd5-47fe-8649-8208f88623a7.png)

-  If we list processes running on the target system using the `ps` command, we see `PID 1304` is `spoolsv.exe` and not `Meterpreter.exe`, as one might expect.

    ![image](https://user-images.githubusercontent.com/63872951/187141167-37baa100-ba10-4142-86d4-ea5334fd4320.png)

- Even if we were to go a step further and look at `DLLs, Dynamic-Link Libraries` used by the Meterpreter process (PID 1304 in this case), we still would not find anything jumping at us (e.g. `no meterpreter.dll`)

  ![image](https://user-images.githubusercontent.com/63872951/187141368-245c61c2-15b5-492f-972b-335073b8148f.png)

- I have not mentioned techniques and tools that can be used to detect Meterpreter. This section aimed to show you how ***stealthy Meterpreter*** is running; remember, **<ins>most antivirus software will detect it</ins>**.

- It is also worth noting that **<ins>Meterpreter will establish an encrypted TLS communication channel with the attacker's system</ins>**.























