## IP Monitor
Whatever openvpn connection you start first, will be tun0 then tun1
<br>
I reccomend starting vpn connection in the same order



# Make sure generic monitor is installed

sudo apt install xfce4-genmon-plugin

# Add generic montior to your panel
<ol>
 <li>Right click panel > Panel > Add New Items</li>
 <li>Search Generic Monitor > add </li>
 <li>Right click Generic Monitor and move to next step </li>
</ol>

#Add Script 
In Command, type the following (gives tun0). In label, add a space then write either HTB ip: or THM ip:
<ul><li>sh -c 'ip a | awk "/tun0\$/{gsub(/\/.*/, \"\"); print \$2}"'</li></ul>
<br><br>
Create another monitor with a separator before (between your last generic monitor and new one)

#Add second Script
In command, type the following (gives tun1). Label with the other label name.
<ul><li>sh -c 'ip a | awk "/tun1\$/{gsub(/\/.*/, \"\"); print \$2}"'</li></ul>
