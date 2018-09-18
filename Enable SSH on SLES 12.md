Run this command:
> systemctl enable sshd.service

Then make necessary changes in your `/etc/ssh/sshd_config` file, and start `sshd` via:
> systemctl start sshd.service

Check if your firewall accepts incoming TCP connections on port 22:
> iptables -nL | grep 22

If the result is empty, you have to add a rule in your firewall.

Open Yast and firewall configuration:
> yast firewall

Goto "Allowed Services" and add "Secure Shell Server". Save and quit Yast and try to connect.

Comment: If you have disabled your firewall completly (not recommended) this answer does not apply.
