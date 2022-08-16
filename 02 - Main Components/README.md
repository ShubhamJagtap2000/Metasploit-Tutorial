# Main Components of Metasploit

- While using the Metasploit Framework, you will primarily interact with the Metasploit Console. You can launch it from the terminal using the `msfconsole` command.

- The console will be your main interface to interact with the different modules of the Metasploit Framework.

- Modules are small components within the Metasploit Framework that are built to perform a specific task, such as exploiting a vulnerability, scanning a target, or performing a brute-force attack. 

- Before diving into **[Modules]()**, it would be helpful to clarify a few recurring concepts: vulnerability, exploit, and payload.

  - **<ins>Exploit</ins>:** A piece of code that uses a vulnerability present on the target system.
  
  - **<ins>Vulnerability</ins>:** A design, coding, or logic flaw affecting the target system. The exploitation of a vulnerability can result in disclosing confidential information or allowing the attacker to execute code on the target system.
  
  - **<ins>Payload</ins>:** An exploit will take advantage of a vulnerability. However, if we want the exploit to have the result we want (gaining access to the target system, read confidential information, etc.), we need to use a payload. Payloads are the code that will run on the target system.
  
- Modules and categories under each one are listed below. These are given for reference purposes, but you will interact with them through the ***[Metasploit Console]() (msfconsole)***.

# Metasploit Modules

  ### 1. [Auxiliary]()
  ### 2. [Encoders]()
  ### 3. [Evasion]()
  ### 4. [Exploits]()
  ### 5. [NOPs]()
  ### 6. [Payloads]()
  ### 7. [Post]()
