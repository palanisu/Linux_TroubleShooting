# Linux_TroubleShooting
# Password Prompt Taking Long
RHEL7:
Symptom: 34 seconds to prompt password ssh login
Solution (my case):
- vi /etc/ssh/sshd_config
- GSSAPIAuthentication no
- service sshd restart

Other Linux versión:
vi /etc/ssh/sshd_config
UseDNS no

vi /etc/resolv.conf
options single-request-reopen ;in the last line. No network restart required
