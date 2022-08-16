# msfconsole

## > Launch Command: `msfconsole`

- Once launched, you will see the command line changes to ***msf5*** (or ***msf6*** depending on the installed version of Metasploit). 

## > ls and ping

- The first command is `ls` which lists the contents of the folder from which Metasploit was launched.
- It is followed by a `ping` sent to Google's DNS IP address (8.8.8.8). 
- We had to add the `-c 1` option, so only a **single** ping was sent. Otherwise, the ping process would continue until it is stopped using `CTRL+C`. 

## > **help**

- While on the subject, the help command can be used on its own or for a specific command. Below is the help menu for the set command we will cover soon.
  
  ![Screenshot (841)](https://user-images.githubusercontent.com/63872951/184949581-50bdd17f-5145-418c-958f-7838318d1ddb.png)

## > history

- You can use the history command to see commands you have typed earlier.
  
  ![Screenshot (843)](https://user-images.githubusercontent.com/63872951/184949625-16d64192-250e-4827-91a7-0d2745c54b01.png)

## > use

- The module to be used can be selected with the use command followed by the number at the beginning of the search result line. 
  
  ![Screenshot (842)](https://user-images.githubusercontent.com/63872951/184950846-fcbffb23-3975-459d-be70-b113c8ca4c5b.png)

## > show

- The prompt tells us we now have a context set in which we will work. You can see this by typing the show options command.

  ![Screenshot (844)](https://user-images.githubusercontent.com/63872951/184951014-a5c1bc74-66c4-4238-b3ac-9f027fa5af39.png)

- The show command can be used in any context followed by a module type (auxiliary, payload, exploit, etc.) to list available modules. The example below lists payloads that can be used with the ms17-010 Eternalblue exploit.

  ![Screenshot (845)](https://user-images.githubusercontent.com/63872951/184951540-22780778-a54a-455e-b2bf-34cc1d0e44af.png)

## > back

- You can leave the context using the back command.

## > info

- Further information on any module can be obtained by typing the info command within its context. 
- Info is not a help menu; it will display detailed information on the module such as its author, relevant sources, etc.

  ![Screenshot (846)](https://user-images.githubusercontent.com/63872951/184951950-e74a8edd-cbcf-4a33-87e6-54442d5f4a37.png)

## > search

- One of the most useful commands in msfconsole is search. This command will search the Metasploit Framework database for modules relevant to the given search parameter. 
- You can conduct searches using CVE numbers, exploit names (eternalblue, heartbleed, etc.), or target system.

  ![Screenshot (847)](https://user-images.githubusercontent.com/63872951/184952551-9def9542-7eed-4f09-9d58-d37bec1c286e.png)

- You can use any module returned in a search result with the command use followed by the number at the beginning of the result line. 

- Another essential piece of information returned is in the `rank` column. 
- Exploits are rated based on their reliability. The table below provides their respective descriptions.

  ![Screenshot (848)](https://user-images.githubusercontent.com/63872951/184953041-ac8ebaf3-fd3d-49c9-973d-3e28cca34f7f.png)

- You can direct the search function using keywords such as type and platform.

- For example, if we wanted our search results to only include auxiliary modules, we could set the type to auxiliary. The screenshot below shows the output of the search     
  ```
  type:auxiliary telnet 
  ```

  ![Screenshot (849)](https://user-images.githubusercontent.com/63872951/184953572-2e7fbd9c-7450-4f5b-9178-beb558f1c96e.png)

- Please remember that exploits take advantage of a vulnerability on the target system and may always show unexpected behavior. 
- A low-ranking exploit may work perfectly, and an excellent ranked exploit may not, or worse, crash the target system.
