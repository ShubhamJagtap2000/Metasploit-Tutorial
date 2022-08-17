# Using Modules

# The exploit Command

- Once all module parameters are set, you can launch the module using the `exploit` command.

- Metasploit also supports the `run` command, which is an alias created for the exploit command as the word exploit did not make sense when using modules that were ***not exploits*** (port scanners, vulnerability scanners, etc.).


- The exploit command can be used ***without*** any parameters or using the `-z` parameter.

- The `exploit -z` command will run the exploit and ***background*** the session as soon as it opens.

  ![Screenshot (854)](https://user-images.githubusercontent.com/63872951/185173633-f846ac5d-6e15-48cc-8c8e-23f9eac49b32.png)

- This will return you the context prompt from which you have run the exploit.

- Some modules support the `check` option. This will **check if the target system is vulnerable without exploiting it**.



