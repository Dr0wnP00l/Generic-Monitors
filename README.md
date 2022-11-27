# IP Monitor
Whatever openvpn connection you start first, will be tun0 then tun1
<br>
I reccomend starting vpn connection in the same order



## Make sure generic monitor is installed

<ul>
 <li>sudo apt install xfce4-genmon-plugin</li>
</ul>

## Add generic montior to your panel
<ol>
 <li>Right click panel > Panel > Add New Items</li>
 <li>Search Generic Monitor > add </li>
 <li>Right click Generic Monitor</li>
 <li>Click Properties</li>
</ol>

## Add Script 
In Command, type the following (gives tun0).
<ul>
 <li>sh -c 'ip a | awk "/tun0\$/{gsub(/\/.*/, \"\"); print \$2}"'</li>
</ul>
<br>
In Label Box:
<ul>
 <li>THM:</li>
</ul>
<br>
*Create another monitor with a separator before (between your last generic monitor and new one)*

## Add second Script
In command, type the following (gives tun1).
<ul>
 <li>sh -c 'ip a | awk "/tun1\$/{gsub(/\/.*/, \"\"); print \$2}"'</li>
</ul>
<br>
In Label Box:
<ul>
 <li>HTB:</li>
</ul>
<br>
