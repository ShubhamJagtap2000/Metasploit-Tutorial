# Sessions

# The background Command

- Once a vulnerability has been ***successfully*** exploited, a session will be created. 
- This is the communication channel established between the `target system and Metasploit`.


- You can use the `background` command to background the session prompt and go back to the msfconsole prompt.
  
  ![Screenshot (855)](https://user-images.githubusercontent.com/63872951/185175431-f2d2c7cf-ad5d-4941-bb0d-7521f0b0eea9.png)

# The sessions Command

- Alternatively, `CTRL + Z` can be used to background sessions.

- The `sessions` command can be used from the ***msfconsole prompt or any context*** to see the existing sessions.

  ![Screenshot (856)](https://user-images.githubusercontent.com/63872951/185176016-06aa1536-fc46-42a7-bc14-ae8c217d6d59.png)

- To interact with any session, you can use the `sessions -i` command followed by the desired session number.

  ![Screenshot (857)](https://user-images.githubusercontent.com/63872951/185176366-9f7d9207-9d9a-426e-9d5a-dab057563201.png)
