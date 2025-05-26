# scan-for-open-ports
Task: Scanning Local Network for Open Ports Using Nmap
    In this task, I performed a port scanning operation on my local network using Nmap, a powerful and widely used network scanning tool.
    The goal was to identify active devices and discover which ports and services are open on those devices, which can help in assessing potential security risks.
Step 1: Running the Nmap Scan
    I began by opening a terminal in Kali Linux and executing the following command:

            sudo nmap -sS 192.168.1.0/24 -oN scan_results.txt
Explanation:
sudo: Runs the command with root privileges, which is required for low-level network scanning.

nmap: The main command to start the Nmap tool.

-sS: Performs a TCP SYN scan, also known as a stealth scan. It is faster and less likely to be detected by firewalls.

192.168.1.0/24: Targets all devices on my local network (from 192.168.1.1 to 192.168.1.254).

-oN scan_results.txt: Saves the scan results in a normal (human-readable) text format to a file named scan_results.txt.


Step 2: Waiting for Scan to Complete
    Nmap scanned the entire local subnet. For each active host it found, 
    it listed the open ports and the services running on those ports. For example, common ports like 22 (SSH) or 80 (HTTP) might be shown as open.

Step 3: Locating the Output File
    After the scan completed, I needed to find where the scan_results.txt file was saved. Since I ran the command from my home directory, I checked it by running:

              pwd
Which showed:
          /home/kali
Then I listed the files using:
              ls
              
And confirmed the file scan_results.txt was present.


Step 4: Viewing the Scan Results
    To read the saved output, I used:

              cat scan_results.txt
This displayed all the IP addresses, open ports, and services discovered during the scan.
I could also open the file with a text editor such as gedit or nano to analyze it more easily.
