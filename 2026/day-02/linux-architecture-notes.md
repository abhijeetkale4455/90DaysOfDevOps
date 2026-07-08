## 1. Linux Architecture

Linux consists of three main components:

### Kernel
- Core part of the operating system.
- Manages CPU, memory, devices, and processes.
- Acts as a bridge between hardware and software.

### User Space
- Area where user applications run.
- Examples: Chrome, VS Code, Bash shell.
- Applications interact with the kernel using system calls.

### systemd
- First process started during boot.
- Has Process ID (PID) 1.
- Manages system services and startup processes.

## process & process Manegement 
 
 Everything in linux is processes ,even a cmd executed by user is process.
- a cmd enter by user on shell.
- shell calls forks() & created a child process.
- child process calls exec().
- kernel schedule it for execution.

# Some of Process state as follow 
Running (R): Process is currently using the CPU.
Sleeping (S): Waiting for an event or input.
Stopped (T): Paused by the user or system.
Zombie (Z): Process has finished but its entry still exists until the parent collects its status.

# Some of important commands for process manegement are as follow
- top: its shows all process used to monitor & troubleshoot
- htop: you can horizontally & vertically scroll all process
- ps -a : is used to display all process
- kill -9 PID: forcefully terminate a process

# systemd
It is a frist process lanuched by kernal,its pid always 1
systemd is the system and service manager in Linux.
It starts services during boot.
It manages background services (daemons).
It can start, stop, restart, and check service status.

-Some of the imp commands of systemd as follow
Check service status:-
    systemctl status ssh
Start a service:-
    Start a service
Stop a service
    sudo systemctl stop nginx
Restart a service
    sudo systemctl restart nginx
Enable service at boot
    sudo systemctl enable nginx
Disable service
    sudo systemctl disable nginx
List running services
    systemctl list-units --type=service

# journalctl
Journalctl displays logs collected by systemd.
View all logs:-
      journalctl
Latest logs:-
      journalctl -xe
Logs for a specific service:-
    journalctl -u nginx


