# SDN-MininetWiFi

This project studies the performance of different SDN controllers in a wireless environment. Here, I use Mininet-WiFi to emulate simple SDNized wireless networks, and I use Ryu and Pox controllers for my study.

# Installation

To install the Mininet-WiFi fork on your system, follow the following steps:

1. Enter the following command: git clone git://github.com/intrig-unicamp/mininet-wifi

2. Go into the Mininet-WiFi folder: cd mininet-wifi

3. Once inside the folder, input the following command: sudo util/install.sh -Wlnfv 

For more information on Mininet-WiFi, refer the official site at https://mininet-wifi.github.io/get-started/ .

To create a single topology with 3 stations, 1 access point, and a remote controller, use the following command:

sudo mn --wifi --topo single,3 --controller=remote

To create a linear topology with 3 stations and 3 stations, 3 access points, and a remote controller, use the following command:

sudo mn --wifi --topo linear,3 --controller=remote

To start the Ryu controller, use the following command:

ryu-manager ryu.app.simple_switch_13

To start the Pox controller, use the following command:

./pox.py log.level --DEBUG forwarding.hub

Use gnuplot to plot the graphs. A useful resource to learn Gnuplot is https://www.youtube.com/watch?v=lGhNL3azDRY&t=833s&ab_channel=WESHARE
