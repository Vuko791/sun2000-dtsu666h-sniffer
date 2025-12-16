Sniffing serial port RS485 Modbus between the Meter DTSU666H and the inverter Huawei Sun2000

Nod-Red flows for listenig and sniffing serial port 485 Modbus between the Meter DTSU666H and the inverter Huawei Sun2000. 

What to buy:
RS485 Wifi or LAN serial port, e.g. ELFIN EW11A Wifi,
Shielded UTP twisted pair internet cable

How to set up Elfin EW11A:

Connect the Elfin Ew11 module to the RS485 Modbus bus between the inverter and the meter A+ to RS485A B- to RS485B.
Connect the Elfin EW11 module to a DC power supply with a voltage of 5V to 18V (DC 5V 500mA power supply).
Use the Elfin setup instructions. Type google.com: elfin ew11 manual pdf .
After logging in to elfin Ew11, select your Wi-Fi network and enter the password (description in the original manual) and reset the Elfin device.
Your router has assigned an IP number in your LAN network for Elfin Ew11, to check it download an application on your phone, e.g. "Net Anlayzer" and scan your network to find the IP number from Elfin.
Access the internal page of Elfin from your web browser by entering its IP in the address bar.
The login and password for Elfin are: admin and admin .

Elfin Ew11 settings:

"System settings tab"- DHCP: Disable DHCP (then Elfin's address on the network will be permanent), WAN IP: Enter the IP address of your Elfin in the LAN network (if the router assigns low IP numbers to devices in the LAN, it is best to assign the Elfin a high number ending, e.g. 192.168.1.200 max 254), Subnet mask: your LAN mask, usually: 255.255.255.0 ("Status" tab to check), Gateway: IP address of your network router which is the gateway to the Internet ("Status" tab to check), DNS: 1.1.1.1 or 8.8.8.8,

"Serial Port tab"- Baund Rate: 9600, Bata bit: 8, Stop bit: 1, Parity: 0, Buffer Size: 512, Gap Time: 50, Cli: Serial String, Srial String: +++, Waiting Toime: 15, Flow control: Disable, Protocol: None,

"Comumunication Settings tab"- Protocol: UDP Client, Serwer: your IP LAN Nod-Red, Server POrt: 2005, Local Port: 2005, Buffer Size: 512, Keep Alive: 60, Timeout: 0, Connect Mode: Always, Register Mode: Disable, Security: Disable, Route: UART,

Submit All and Restart Elfin EW11

Go to the Elfin internet address with the new IP, ending with the number you assigned. The UDP port 2005 is activated anh binary data sends do NodRed on port 2005.
