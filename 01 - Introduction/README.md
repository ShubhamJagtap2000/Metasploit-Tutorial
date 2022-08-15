# Introduction to Metasploit

- Metasploit is the most widely used exploitation framework. Metasploit is a powerful tool that can support all phases of a penetration testing engagement, from information gathering to post-exploitation.

- Metasploit has two main versions:

    - **Metasploit Pro:** The commercial version that facilitates the automation and management of tasks. This version has a ***graphical user interface (GUI)***.
    - **Metasploit Framework:** The open-source version that works from the command line. This room will focus on this version, installed on the AttackBox and most commonly used penetration testing Linux distributions.4

- The Metasploit Framework is a set of tools that allow information gathering, scanning, exploitation, exploit development, post-exploitation, and more. 
- While the primary usage of the Metasploit Framework focuses on the penetration testing domain, it is also useful for vulnerability research and exploit development.

- The main components of the Metasploit Framework can be summarized as follows:

    - **msfconsole:** The main command-line interface.
    - **Modules:** supporting modules such as exploits, scanners, payloads, etc.
    - **Tools:** Stand-alone tools that will help vulnerability research, vulnerability assessment, or penetration testing. Some of these tools are ***msfvenom, pattern_create and pattern_offset***. We will cover msfvenom within this repository, but ***pattern_create*** and ***pattern_offset*** are tools useful in exploit development which is beyond the scope of this module. 

