---
Title: SWS101_Linux_Commands
categories: [SWS101, Journal 1]
tags: [SWS101]
---



## Bandit - OverTheWire Game Notes

### Level 0
Teaches how to use the ssh (secure shell) command to access another server. In this level, I am introduced to basic server access protocols and provided with the initial credentials to connect to the Bandit server. I need the username, IP address and the password to log in on the bandit game. i connect by using the host 'bandit.labs.overthewire.org' on port 2220

- command line
![Alt text](../image/ssh.png)


### Level 1
Introduced basic Linux commands for directing directories. I learn commands like ls to list directory contents and cd to change directories. In this level we required to discover the password for the next level, and it’s hidden in a file called “readme” within the home directory. I tried the “cat” command, and it worked. This command helps concatenates files and also display what’s inside them.

### Level 2
Highlighted the necessity of using backslashes (`/`) to handle spaces in filenames. This level emphasizes the importance of escaping special characters in filenames to properly interact with files in the Linux environment.

### Level 3
Introduced the command ls -a to find hidden files in directories. Here, I learn that files starting with a dot (`.`) are considered hidden and are not displayed by default in directory listings.

### Level 4
Learned a shortcut to identify human-readable or specific types of files. I learn to use commands like file to quickly identify file types based on their content or metadata.

### Level 5
Similar to Level 4, but required specifying detailed file attributes. I am challenged to use commands like file with additional flags to identify specific file types or attributes.

### Level 6
Focused on specifying detailed file attributes to find a password. I learn to use commands like file and grep to search for specific patterns within files and extract relevant information.

### Level 7
Introduced the grep command to search for specific patterns within files. Here, I learn to use regular expressions and flags with grep to perform more complex searches and pattern matching.

### Level 8
Utilized commands like uniq and sorting to find unique characters in a password. I am challenged to analyze text files, identify unique characters, and extract the password using command-line tools.

### Level 9
Applied the grep command to search for specific lines of characters. I learn to use grep with patterns to extract specific lines containing passwords or other relevant information from text files.

### Level 10
Encountered base64 encoding and learned how to decode it. I learn about common encoding schemes like base64 and how to decode encoded data to retrieve passwords or other hidden information.

### Level 11
Utilized the concept of rot13 and the tr command to decode passwords. Here, I learn about simple substitution ciphers like rot13 and how to use text manipulation tools like tr to decode encoded passwords.

### Level 12
Learned to decompress files to access their contents. I encounter compressed files and learn to use commands like gzip and tar to decompress them and access the contents within.

### Level 13
Used an SSH key file to log in to another level. I learn about SSH key-based authentication and how to use private key files to securely authenticate with remote servers.

### Level 14
Introduced the nc (netcat) command for communication over specific ports. I learn about network sockets and how to use nc to establish connections and communicate with services running on specific ports.

### Level 15
Introduced the ssl command for establishing secure connections. I learn about SSL/TLS encryption and how to use the ssl command to establish secure connections with servers over the network.

### Level 16
Learned to use nmap for scanning open ports and identifying services, particularly SSL-encrypted ones. I learn about network scanning techniques and how to use nmap to gather information about remote servers and their services.

### Level 17
Utilized the diff command to find changes between files and extract passwords. I learn to compare text files and identify differences between them, extracting passwords or other hidden information from changed lines.

### Level 18
Resolved a challenge involving modifications to the .bashrc file by using ssh with the -t option to access a file affected by these modifications. I learn about the .
bashrc file and how to access files affected by shell configuration changes using ssh with the -t option.

### Level 19
Learned to run commands as another user using the bandit20-do program, which bypasses usual permission restrictions. I encounter privilege escalation challenges and learn to execute commands with elevated privileges using special programs like bandit20-do.

### Level 20
Encountered the suconnect program, which connects to a specific port on my computer and verifies passwords to grant access to the next level. I learn about custom services and how to interact with them using network utilities like suconnect to progress to the next level.