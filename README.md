### IP Monitor

## Whatever openvpn connection you start first, will be tun0 then tun1
## I reccomend starting vpn connection in the same order



# Make sure generic monitor is installed

sudo apt install xfce4-genmon-plugin

# Add generic montior to your panel

# In Command, type the following (gives tun0). In label, add a space then write either HTB ip: or THM ip:
sh -c 'ip a | awk "/tun0\$/{gsub(/\/.*/, \"\"); print \$2}"'

# Create another monitor with a separator before (between your last generic monitor and new one)

#In command, type the following (gives tun1). Label with the other label name.
sh -c 'ip a | awk "/tun1\$/{gsub(/\/.*/, \"\"); print \$2}"'
