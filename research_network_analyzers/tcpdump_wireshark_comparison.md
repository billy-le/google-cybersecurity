## Wireshark Features

- troubleshoot network problems
- capture live packet data from a network device
- save and open p-caps files
- import packets from text files containing hex dumps of packet data
- export packets in various capture file formats
- search and filter packets on many criteria
- colorized packets
- open source
- uses a graphical user interface

## tcpdump Features

- lightweight, usually already installed on linux-based systems
- can capture real-time packets on network interfaces
- can read pcap files
- uses command-line interface
- can search and filter for packets
- can be used in remote environments by ssh'ing into a remote server

## Comparison

- Wireshark uses a GUI while tcpdump only works in the terminal
- tcpdump can be used in a remote setting whereas Wireshark cannot
- Wireshark is widely available on different platforms while tcpdump is only on unix-based systems
- Wireshark can decrypt packets if there are keys available, tcpdump does not have this feature
- Wireshark is good for complex filters, tcpdump is good for simple filters
