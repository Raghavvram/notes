# Linux Commands

**Last Updated:** 2025-07-15

This file contains a list of common Linux commands, categorized by their function.

## File Management

*   `ls`: Lists files and directories.
*   `cd`: Changes the current directory.
*   `pwd`: Prints the current working directory.
*   `mkdir`: Creates a new directory.
*   `rm`: Removes files or directories.
*   `cp`: Copies files or directories.
*   `mv`: Moves or renames files or directories.
*   `touch`: Creates a new empty file.
*   `cat`: Concatenates and displays file contents.
*   `less`: Views file contents page by page.
*   `head`: Displays the first few lines of a file.
*   `tail`: Displays the last few lines of a file.
*   `echo`: Displays a line of text or writes text to a file.

## Searching and Finding Files

*   `find`: Searches for files and directories based on specified criteria.
*   `grep`: Searches for patterns within files.

## User Management

*   `adduser`: Adds a new user with a home directory and default settings.
*   `useradd`: Adds a new user without default settings.
*   `usermod`: Modifies user account properties.
*   `passwd`: Sets or changes user passwords.
*   `whoami`: Displays the current logged-in user.
*   `id`: Displays user and group IDs.
*   `deluser`: Removes a user account.

## Ownership and Permissions

*   `chown`: Changes file ownership.
*   `chmod`: Changes file permissions.
*   `umask`: Sets default file creation permissions.

## Networking

*   `ping`: Tests the connection to a host.
*   `traceroute`: Shows the route packets take to a network host.
*   `ifconfig`: Configures or displays network interface parameters.
*   `ip`: Manages IP addresses, routes, and network interfaces.
*   `nmap`: Scans networks to discover hosts and services.
*   `tcpdump`: Captures and analyzes network packets.
*   `curl`: Transfers data from or to a server.
*   `arp-scan`: Uses ARP packets to identify devices on your local network.
*   `netdiscover`: Maps out active hosts within your subnet.
*   `fping`: A faster version of ping that sends ICMP echo requests to multiple hosts simultaneously.
*   `masscan`: Scans the entire internet in minutes to reveal open ports.

## Security

*   `fail2ban`: Scans logs for repeated failed login attempts and blocks the attacking IP addresses.
*   `iptables`: A firewall configuration tool to control incoming and outgoing traffic.
*   `ufw`: A user-friendly alternative to iptables.
*   `hydra`: A tool for brute force cracking of various protocols.
*   `nikto`: Scans web servers for potential security vulnerabilities.
*   `gobuster`: Scans directories and performs brute force attacks against web servers.
*   `Burp Suite`: A suite for testing and interacting with web applications.
*   `sqlmap`: Probes databases for vulnerabilities.
*   `dirb`: Discovers hidden directories and files.

## System Monitoring and Management

*   `dstat`: Shows detailed information on CPU, memory, disk, and network usage in real-time.
*   `iostat`: Provides input/output statistics for devices.
*   `pstree`: Visually organizes running processes in a tree format.
*   `iftop`: Monitors network bandwidth in real-time.
*   `tcpflow`: Captures and inspects data flowing over TCP connections.
*   `wireshark`: A network protocol analyzer that captures and dissects raw data of network traffic.
*   `lsof`: Lists open files by processes.
*   `htop`: An interactive process viewer.
*   `nice`: Adjusts process priority.
*   `renice`: Modifies the priority of running processes.

## Automation and Scheduling

*   `cron`: Schedules tasks to run at specified intervals.
*   `at`: Schedules one-time tasks.
*   `watch`: Executes a command at regular intervals and displays the output.
*   `sleep`: Pauses execution for a specified amount of time.

## Text Processing

*   `awk`: A powerful text processing language.
*   `sed`: A stream editor for filtering and transforming text.
*   `tr`: Translates or deletes characters.
*   `cut`: Removes sections from each line of files.