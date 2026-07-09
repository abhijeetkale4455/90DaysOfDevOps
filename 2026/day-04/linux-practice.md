# Linux Practice:Processes and Service

# Process Checks
- 1. Show All Running Processes 
 
   ps -ef 

   ![alt text](image.png)

- 2. Show Frist few running processes 

   ps -ef | head

   ![alt text](image-1.png)

- 3. Find a specific Process

  ps -ef | grep sshd

      ![alt text](image-2.png)
    

##  Service Checks

- 1. Check SSH Service Status
  Syntax :- 
        systemctl status sshd

    ![alt text](image-3.png)


## Log Checks

- 1. Check SSH Logs

  journalctl -u sshd -n 10

