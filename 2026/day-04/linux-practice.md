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
    

##  Systemd Coomands

-  Check SSH Service Status
  Syntax :- 
        systemctl status sshd

    ![alt text](image-3.png)

-  systemctl list-units

      ![alt text](image-4.png)

- journalctl

   ![alt text](image-5.png)

- journalctl -u docker |tail -n 15

      ![alt text](image-7.png)




