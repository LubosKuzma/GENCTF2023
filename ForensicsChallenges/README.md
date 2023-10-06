# Forensics Challenges List

## 1. Log Analysis
- **Description**: Provided with a system or application log file, participants need to identify anomalous activities or signs of attacks and answer related questions.
- **Tools**: Log analysis tools, text processing tools like `grep`, `awk`, `sed`, etc.

## 2. Memory Forensics
- **Description**: Given a memory dump, participants need to extract information about malware or attacker activities.
- **Tools**: `Volatility`, `Rekall`, etc.

## Challenge 3 （Network Forensics）
- **Category**: Forensics
- **Description**: Provided with a network traffic capture file (e.g., PCAP), participants need to analyze the traffic for signs that hides secret information.
- **Flag**: genctf{TH1S_1S_@_5ECRET}
- **Tools**: `Wireshark`, `tcpdump`, `tshark`, etc.
- **Quick Guide**: For Wireshark, use Statistics --> Conversations --> TCP --> use Follow Stream check each stream --> we can find the hidden message in the tcp.stream eq 1 --> ROT 13 --> final flag
- **hint**: N/A

## 4. File System and Disk Analysis
- **Description**: Given a disk image, participants need to analyze the filesystem structure, metadata, hidden partitions, etc., to uncover hidden or deleted data.
- **Tools**: `The Sleuth Kit (TSK)`, `Autopsy`, `binwalk`, etc.

## Challenge 5 （Mobile Forensics）
- **Description**: Provided with a backup or image of a mobile device (Android), participants need to extract app data, messages, call logs, contacts, or other hidden information.
- **Flag**: genctf{53cr3tM!ss!0n@Ph0n3}
- **Tools**: `SQLite Database Browser`, `grep`, `strings`, etc.
- **Quick Guide**: Extract the provided data_backup.tar file to access the contents -->  Locate the SMS database file, found in `/data/data/com.android.providers.telephony/databases/mmssms.db` --> Use SQLite Database Browser to open the database file --> Browse through the tables and records to find the messages --> Look for unusual or encoded messages that could hide the flag
- **hint**: Some messages are meant to be read and deleted immediately.

  
## 6. Database Forensics
- **Description**: Given a database backup or image, like MySQL, PostgreSQL, MongoDB, etc., participants need to analyze the data, uncover deleted or hidden records, or recover data from logs.
- **Tools**: Database-specific query tools, `SQL parsers`, `database log analyzers`, etc.
