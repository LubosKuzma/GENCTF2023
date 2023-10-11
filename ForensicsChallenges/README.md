# Forensics Challenges List

## 1. Log Analysis
- **Description**: Provided with a system or application log file, participants need to identify anomalous activities or signs of attacks and answer related questions.
- **Tools**: Log analysis tools, text processing tools like `grep`, `awk`, `sed`, etc.

## 2. Memory Forensics
- **Category**: Forensics
- **Description**: Given a memory dump, participants need to extract information about the registry and process including attacker activities.
- **Flag**: genctf{2023_TWVt60ryRHVt@_Win}
- **Tools**: `Volatility`, `strings`, `Rekall`, etc.
- **Quick Guide**: (Volatility 2)
###1) Profile Identification: Run the command `volatility -f Forensics_Challenge_2.mem imageinfo` to identify the correct profile for the memory dump using the imageinfo plugin in the Volatility Framework -->
###2) Registry Hive Listing: List the registry hives in the memory dump using the hivelist plugin by executing the command `volatility -f Forensics_Challenge_2.mem --profile=Win7SP1x64 hivelist` -->
###3) Keyword Search: Use strings to find a keyword by executing the command `strings Forensics_Challenge_2.mem | grep -i "genctf"`. The output shows Software\GenCTF indicating a potential registry key of interest -->
###4) Registry Key Inspection: In the hivelist output, locate the `\SystemRoot\System32\Config\SOFTWARE` Virtual address. Use the printkey plugin to inspect a specific registry key by executing the command `volatility -f Forensics_Challenge_2.mem --profile=Win7SP1x64 printkey -o 0x0000f8a00011f010 -K "GenCTF"`, leading to the discovery of flag_part1 -->
###5) Process Listing: Use the pslist command to list all running processes and take note of any unusual or unknown processes by executing the command `volatility -f Forensics_Challenge_2.mem --profile=Win7SP1x64 pslist`, find the suspicious process win7pre.exe and determine its PID -->
###6) Process Memory Extraction: Utilize the memdump plugin to extract the memory of the identified process by executing the command `volatility -f Forensics_Challenge_2.mem --profile=Win7SP1x64 memdump -p 2856 -D output_directory`. This command will create a memory dump file for the process with PID 2856 and save it in the output_directory -->
###7) Flag Search: Use strings to search for the flag by executing the command `strings 2856.dmp | grep "flag"`, iterate through the findings to locate flag_part2, then combine the two parts into the genctf{xxxxxx} format to obtain the complete flag  
- **Hint**: Your journey will demand a keen eye for anomalies within the registry and running processes. Happy hunting!

## Challenge 3 （Network Forensics）
- **Category**: Forensics
- **Description**: Provided with a network traffic capture file (e.g., PCAP), participants need to analyze the traffic for signs that hides secret information.
- **Flag**: genctf{TH1S_1S_@_5ECRET}
- **Tools**: `Wireshark`, `tcpdump`, `tshark`, etc.
- **Quick Guide**: For Wireshark, use Statistics --> Conversations --> TCP --> use Follow Stream check each stream --> we can find the hidden message in the tcp.stream eq 1 --> ROT 13 --> final flag
- **Hint**: N/A

## 4. File System and Disk Analysis
- **Description**: Given a disk image, participants need to analyze the filesystem structure, metadata, hidden partitions, etc., to uncover hidden or deleted data.
- **Tools**: `The Sleuth Kit (TSK)`, `Autopsy`, `binwalk`, etc.

## Challenge 5 （Mobile Forensics）
- **Description**: Provided with a backup or image of a mobile device (Android), participants need to extract app data, messages, call logs, contacts, or other hidden information.
- **Flag**: genctf{53cr3tM!ss!0n@Ph0n3}
- **Tools**: `SQLite Database Browser`, `grep`, `strings`, etc.
- **Quick Guide**: Extract the provided data_backup.tar file to access the contents -->  Locate the SMS database file, found in `/data/data/com.android.providers.telephony/databases/mmssms.db` --> Use SQLite Database Browser to open the database file --> Browse through the tables and records to find the messages --> Look for unusual or encoded messages that could hide the flag
- **Hint**: Some messages are meant to be read and deleted immediately.

  
## 6. Database Forensics
- **Description**: Given a database backup or image, like MySQL, PostgreSQL, MongoDB, etc., participants need to analyze the data, uncover deleted or hidden records, or recover data from logs.
- **Tools**: Database-specific query tools, `SQL parsers`, `database log analyzers`, etc.
