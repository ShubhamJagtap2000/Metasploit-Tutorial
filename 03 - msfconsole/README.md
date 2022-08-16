# msfconsole

### > Launch Command: `msfconsole`

- Once launched, you will see the command line changes to ***msf5*** (or ***msf6*** depending on the installed version of Metasploit). 

### > ls and ping

- The first command is `ls` which lists the contents of the folder from which Metasploit was launched.
- It is followed by a `ping` sent to Google's DNS IP address (8.8.8.8). 
- We had to add the `-c 1` option, so only a **single** ping was sent. Otherwise, the ping process would continue until it is stopped using `CTRL+C`. 

### > **help**

- While on the subject, the help command can be used on its own or for a specific command. Below is the help menu for the set command we will cover soon.
  
  ![Screenshot (841)](https://user-images.githubusercontent.com/63872951/184949581-50bdd17f-5145-418c-958f-7838318d1ddb.png)

### > history

- You can use the history command to see commands you have typed earlier.
  
  ![Screenshot (843)](https://user-images.githubusercontent.com/63872951/184949625-16d64192-250e-4827-91a7-0d2745c54b01.png)

### > use

- The module to be used can be selected with the use command followed by the number at the beginning of the search result line. 
  
  ![Screenshot (842)](https://user-images.githubusercontent.com/63872951/184950846-fcbffb23-3975-459d-be70-b113c8ca4c5b.png)

### > show

- The prompt tells us we now have a context set in which we will work. You can see this by typing the show options command.

  ![Screenshot (844)](https://user-images.githubusercontent.com/63872951/184951014-a5c1bc74-66c4-4238-b3ac-9f027fa5af39.png)

- The show command can be used in any context followed by a module type (auxiliary, payload, exploit, etc.) to list available modules. The example below lists payloads that can be used with the ms17-010 Eternalblue exploit.

  ![Screenshot (845)](https://user-images.githubusercontent.com/63872951/184951540-22780778-a54a-455e-b2bf-34cc1d0e44af.png)

### > back

- You can leave the context using the back command.

### > info

- Further information on any module can be obtained by typing the info command within its context. 
- Info is not a help menu; it will display detailed information on the module such as its author, relevant sources, etc.

  ![Screenshot (846)](https://user-images.githubusercontent.com/63872951/184951950-e74a8edd-cbcf-4a33-87e6-54442d5f4a37.png)

### > search
