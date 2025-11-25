## Brief explanations of your problem-solving approach:
While completing this module, I used a practical, step-by-step approach to build my command-line skills. I started by learning the fundamentals in TryHackMe and Linux Journey, focusing on understanding why each command works rather than memorizing syntax. I practiced each new command directly in the terminal to build confidence and familiarity.

For exercises in OverTheWire Bandit, I approached each level as a small security challenge. I broke down the problem, identified useful commands, tested different options, and used tools like man, --help, and careful observation to find solutions. When issues came up, I troubleshot by checking file paths, permissions, and context until I understood the root cause.

## Reflection on what you learned and found challenging:

<img width="1910" height="399" alt="linux 1" src="https://github.com/user-attachments/assets/e26d8d96-39c8-471c-9f25-0e9a03f3880f" />
<img width="1907" height="786" alt="linux 2" src="https://github.com/user-attachments/assets/0e0c08af-eea9-4a0b-9c46-522a3cdfad95" />


### Linux Commands
| Command                                       | Description        |
|-----------------------------------------------|----------------------------|
| echo                                          | Write input text to standard output |
| whoami                                        | Display info about the user currently logged in |
| pwd                                           | Display pathname of the current working directory |
| ls                                            | Display/list contents of a directory |
| cd                                            | Navigate between directories |
| cat                                           | Display, concatenate, create, or append files |
| cp                                            | Copy files and directories |
| mv                                            | Rename or move files and directories |
| mkdir                                         | Create new directory |
| rm                                            | Remove files and directories |
| touch                                         | Update access and modify timestamps for existing files; if the file does not exist it can create a new file |
| find                                          | Search for files or directories within a specific location |
| grep                                          | Search for text patterns within a specific file |
| strings                                       | Extracts and displays sequences of printable characters from files |
| file                                          | Display file type |
| less                                          | Display text files or output in paged format |
| history                                       | Display history of used commands |
| gzip                                          | Reduce file size by replacing the original file with a compressed version ending in .gz |
| help                                          | Provide info about Bash built-in commands |
| man                                           | Provide info about commands, their flags/options, and how they're used |
| whatis                                        | Provide one-line description of a command from its man page |
| alias                                         | Create a custom name for any command or sequence of commands |
| exit                                          | Terminates current shell session |

### Linux Operators
| Command                                       | Description        |
|-----------------------------------------------|----------------------------|
| &                                             | Run command in the background  |
| &&                                            | Chain commands together conditionally |
| >                                             | Redirect standard output of a command to a file, overwrites existing file |
| >>                                            | Redirect standard output of a command to a file, but appends the output instead |

***
<img width="1920" height="400" alt="windows 1" src="https://github.com/user-attachments/assets/17dbb180-43a8-40b1-8f8b-a5e2ab4270fd" />

### Windows Commands
| Command                                       | Description        |
|-----------------------------------------------|----------------------------|
| set                                           | Create, modify, or display environment variables for the current command prompt session |
| ver                                           | Display the operating system (OS) version. |
| systeminfo                                    | Display detailed configuration and hardware information about the local or a remote computer |
| more                                          | Display a text file or the output of another command in page format |
| driverquery                                   | Display a list of all device drivers installed on the system |
| help                                          | Provide help information for a specific command |
| cls                                           | Clear the Command Prompt screen |
| ipconfig                                      | Display and manage a computer's current network configuration |
| ping                                          | Test network connectivity by sending an Internet Control Message Protocol (ICMP) echo request to a specific IP address or domain name |
| tracert                                       | Determines the route to a destination by sending ICMP packets and tracking the number of hops a packet takes to reach its destination |
| nslookup                                      | Query the Domain Name System (DNS) to obtain IP addresses for domain names or vice versa |
| netstat                                       | Display network statistics, connections, and listening ports |
| cd                                            | Display current directory or navigate between directories |
| dir                                           | Display a list of files and subdirectories within a specified directory |
| tree                                          | Display graphically, the directory structure of a specified path or drive |
| mkdir                                         | Create new directory |
| rmdir                                         | Remove a directory |
| type                                          | Display the contents of a text file directly in the command-line window |
| copy                                          | Create a copy of a file or combine multiple files into a single new file |
| del/erase                                     | Remove files and directories |
| *                                             | Refer to multiple files |
| tasklist                                      | Display a list of all currently running processes on a local or remote computer |
| tasklist /FI                                  | Display a list of all currently running processes on a local or remote computer, filtered by specific criteria |
| taskkill                                      | Terminate one or more running processes |
| /?                                            | Displays the syntax and a description of a command |
| shutdown                                      | Shutdown, restart, or log off a computer locally or remotely |

***
<img width="1911" height="425" alt="windows 2" src="https://github.com/user-attachments/assets/595e1529-2bcb-4b21-89da-1cb9f2b41578" />

### Windows Versions:
Windows 1.0 - 1985
Windows XP - 2001
Windows 7 - 2009
Windows 10 - 2015
Windows 11 - 2021

### Windows GUI:
- The Desktop
- Start Menu
- Search Box (Cortana)
- Task View
- Taskbar
- Toolbars
- Notification Area

### Windows File System:
- File Allocation Table (FAT16/FAT32)
- High Performance File System (HPFS)
- New Technology File System (NTFS)

### New Technology File System Permissions:
- Full control
- Modify
- Read & Execute
- List folder contents
- Read
- Write

### Windows/System32 Folders
- Environment variables store information about the operating system environment. This information includes details such as the operating system path, the number of processors used by the operating system, and the location of temporary folders.
- The system  environment variable for the Windows directory is %windir%.
- The System32 folder holds the important files that are critical for the operating system. You should proceed with extreme caution when interacting with this folder. Accidentally deleting any files or folders within System32 can render the Windows OS inoperational.

### User Accounts, Profiles, and Permissions
- An Administrator can make changes to the system: add users, delete users, modify groups, modify settings on the system, etc. 
- A Standard User can only make changes to folders/files attributed to the user & can't perform system-level changes, such as install programs.
- Right-click on the Start Menu and click Run, then type lusrmgr.msc to open Local Users and Management
- User Account Control (UAC)

### Settings, Control Panel, and Task Manager
- The Settings menu was introduced in Windows 8, the first Windows operating system catered to touch screen tablets, and is still available in Windows 10. As a matter of fact, the Settings menu is now the primary location a user goes to if they are looking to change the system. 
- Control Panel is the menu where you will access more complex settings and perform more complex actions. In some cases, you can start in Settings and end up in the Control Panel.
- The Task Manager provides information about the applications and processes currently running on the system. Other information is also available, such as how much CPU and RAM are being utilized, which falls under Performance. The keyboard shortcut to Task Manager is Ctrl+Shift+Esc.

## Questions or areas where you'd like additional clarification:

