# 🎯 Networking & Red Hat Enterprise Linux (RHEL) Interview Questions — Part 11 (Questions Only)

> **Scope:**
> **Part A — Networking:** OSI & TCP/IP models, IP addressing & subnetting, IPv6, ports & protocols, TCP/UDP internals, DNS, DHCP, ARP, routing & switching, NAT, VLANs, HTTP/HTTPS/TLS, proxies & load balancers, firewalls, VPNs, cloud networking (VPC), container & Kubernetes networking, network security, troubleshooting tools.
> **Part B — Red Hat Enterprise Linux:** Linux fundamentals, RHEL specifics, file system & permissions, users & groups, processes & signals, systemd & services, package management (dnf/yum/rpm), storage (LVM, partitions, mounts, XFS), networking on RHEL (nmcli, NetworkManager), **firewalld**, **SELinux**, SSH, logs (journald, rsyslog), scheduling (cron, systemd timers), shell scripting, performance troubleshooting, boot process, security hardening, Podman/containers, and **hosting .NET + Nginx on RHEL**.
> **Based on question patterns from:** product MNCs, service MNCs, financial-domain companies (banks run heavily on RHEL), mid-level product companies and startups, plus questions candidates commonly report on LinkedIn and Glassdoor. Linux questions are aligned with RHEL 8/9/10 and RHCSA topics.

**Legend:** 🟢 Fresher (0–2 yrs) · 🟡 Mid-level (2–5 yrs) · 🔴 Senior (5+ yrs) · 💰 Frequently asked in financial-domain companies

---

## 📚 Table of Contents

**Part A — Networking**
1. Networking Fundamentals
2. OSI Model & TCP/IP Model
3. IP Addressing, Subnetting & CIDR
4. IPv6
5. Ports & Common Protocols
6. TCP Deep Dive
7. UDP & QUIC
8. DNS
9. DHCP, ARP & ICMP
10. Switching, Routing, VLANs & NAT
11. HTTP, HTTPS & TLS
12. Proxies, Load Balancers & CDNs
13. Firewalls, VPNs & Network Security
14. Cloud Networking (VPC, Subnets, Security Groups)
15. Container & Kubernetes Networking
16. Network Troubleshooting Tools

**Part B — Red Hat Enterprise Linux**
17. Linux & RHEL Fundamentals
18. File System Hierarchy & Basic Commands
19. Text Processing & Searching
20. File Permissions, Ownership, ACLs & Special Permissions
21. Users, Groups & sudo
22. Processes, Jobs & Signals
23. systemd, Services & Targets
24. Package Management (dnf, yum, rpm, repositories, subscription)
25. Storage — Disks, Partitions, Filesystems, Mounts, fstab
26. LVM (Logical Volume Manager) & Stratis
27. Networking on RHEL (NetworkManager, nmcli, ip, ss)
28. firewalld
29. SELinux
30. SSH & Remote Access
31. Logging — journald, rsyslog, logrotate
32. Scheduling — cron, at, systemd timers
33. Shell Scripting (Bash)
34. Performance Monitoring & Troubleshooting
35. Boot Process, GRUB & Recovery
36. Security Hardening & Compliance
37. Containers on RHEL — Podman, Buildah, Skopeo
38. Hosting .NET & Nginx on RHEL

**Part C — Practice**
39. Financial-Domain Questions 💰
40. Tricky Questions
41. Predict the Output (Commands & Configs)
42. Scenario-Based Questions — Networking
43. Scenario-Based Questions — Linux / RHEL Production Issues
44. Hands-On Tasks
45. Rapid-Fire Round

---

# Part A — Networking

## 1. Networking Fundamentals

1. 🟢 What is a computer network?
2. 🟢 What are LAN, WAN, MAN and PAN?
3. 🟢 What is the difference between the internet, an intranet and an extranet?
4. 🟢 What are network topologies (bus, star, ring, mesh, hybrid)?
5. 🟢 What is a host, a node, a client and a server?
6. 🟢 What is bandwidth? What is throughput? What is latency? What is jitter?
7. 🟢 What is packet loss?
8. 🟢 What is the difference between a hub, a switch and a router?
9. 🟢 What is a modem? What is a gateway?
10. 🟡 What is unicast, broadcast, multicast and anycast?
11. 🟡 What is half-duplex vs full-duplex?
12. 🟡 What is MTU? What happens when a packet is larger than the MTU (fragmentation)?
13. 🟡 What is circuit switching vs packet switching?
14. 🟡 What is a MAC address? How is it different from an IP address?

---

## 2. OSI Model & TCP/IP Model

15. 🟢 What is the OSI model? Name all 7 layers.
16. 🟢 What is the responsibility of each OSI layer?
17. 🟢 What is the TCP/IP model? How do its 4 layers map to OSI?
18. 🟡 At which layer do switches, routers, firewalls and load balancers operate?
19. 🟡 At which layer do HTTP, TLS, TCP, IP, Ethernet and ARP operate?
20. 🟡 What is encapsulation and decapsulation?
21. 🟡 What are PDUs at each layer (data, segment, packet, frame, bits)?
22. 🟡 What happens at each layer when you open a website?
23. 🔴 Why is TLS hard to place in the OSI model?

---

## 3. IP Addressing, Subnetting & CIDR

24. 🟢 What is an IP address? What is IPv4?
25. 🟢 What are IPv4 address classes (A, B, C, D, E)?
26. 🟢 What are private IP ranges (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16)?
27. 🟢 What is a public IP vs a private IP?
28. 🟢 What is 127.0.0.1 (loopback)? What is 0.0.0.0?
29. 🟢 What is a subnet mask?
30. 🟡 What is CIDR notation? What does /24 mean?
31. 🟡 How many usable hosts are in a /24, /26, /28 and /16 subnet?
32. 🟡 What is the network address and broadcast address of a subnet?
33. 🟡 Divide 192.168.10.0/24 into 4 equal subnets. What are their ranges?
34. 🟡 Is 10.0.5.20 in the subnet 10.0.4.0/23?
35. 🟡 What is a default gateway?
36. 🟡 What is APIPA (169.254.x.x)?
37. 🟡 What is supernetting / route summarisation?
38. 🔴 How would you plan IP ranges for a VPC with public, private and database subnets across 3 availability zones?

---

## 4. IPv6

39. 🟢 What is IPv6? Why was it introduced?
40. 🟡 What is the format of an IPv6 address? How do you shorten it?
41. 🟡 What are IPv6 address types (global unicast, link-local, unique local, multicast, anycast)?
42. 🟡 What is `::1`?
43. 🟡 What is SLAAC?
44. 🟡 What are the main differences between IPv4 and IPv6 (no broadcast, no NAT needed, header changes)?
45. 🔴 What is dual-stack? What problems can it cause for applications?

---

## 5. Ports & Common Protocols

46. 🟢 What is a port? What is a socket?
47. 🟢 What are well-known, registered and ephemeral ports?
48. 🟢 Which ports do these use: HTTP, HTTPS, SSH, FTP, SFTP, SMTP, DNS, DHCP, RDP, SQL Server, MySQL, PostgreSQL, Oracle, Redis, MongoDB, Kafka, RabbitMQ, LDAP, NTP?
49. 🟡 What is the difference between FTP, FTPS and SFTP?
50. 🟡 What are SMTP, POP3 and IMAP?
51. 🟡 What is SNMP?
52. 🟡 What is NTP and why is time synchronisation important for servers? 💰
53. 🟡 What is LDAP?
54. 🟡 What is the ephemeral port range on Linux and what is ephemeral port exhaustion?

---

## 6. TCP Deep Dive

55. 🟢 What is TCP? What guarantees does it provide?
56. 🟢 Explain the TCP three-way handshake (SYN, SYN-ACK, ACK).
57. 🟢 Explain the TCP four-way connection termination (FIN, ACK).
58. 🟡 What are TCP states (LISTEN, SYN_SENT, SYN_RECEIVED, ESTABLISHED, FIN_WAIT_1/2, CLOSE_WAIT, TIME_WAIT, LAST_ACK, CLOSED)?
59. 🟡 What is TIME_WAIT? Why does it exist? Why can too many TIME_WAIT connections be a problem?
60. 🟡 What does a large number of CLOSE_WAIT connections indicate?
61. 🟡 What are sequence numbers and acknowledgements?
62. 🟡 What is flow control (sliding window)?
63. 🟡 What is congestion control (slow start, congestion avoidance)?
64. 🟡 What is a TCP retransmission?
65. 🟡 What is Nagle's algorithm? What is `TCP_NODELAY`?
66. 🟡 What is TCP keep-alive vs HTTP keep-alive?
67. 🟡 What is a TCP RST (reset)? When is it sent?
68. 🔴 What is a SYN flood attack? How do SYN cookies help?
69. 🔴 What is head-of-line blocking in TCP?

---

## 7. UDP & QUIC

70. 🟢 What is UDP?
71. 🟢 What is the difference between TCP and UDP?
72. 🟢 Which applications use UDP (DNS, video streaming, gaming, VoIP)? Why?
73. 🟡 How can reliability be built on top of UDP?
74. 🟡 What is QUIC? Why does HTTP/3 use it?
75. 🟡 How does QUIC avoid head-of-line blocking?

---

## 8. DNS

76. 🟢 What is DNS? Why do we need it?
77. 🟢 What happens during DNS resolution (recursive resolver, root, TLD, authoritative)?
78. 🟢 What are DNS record types (A, AAAA, CNAME, MX, TXT, NS, SOA, PTR, SRV, CAA)?
79. 🟡 What is the difference between an A record and a CNAME?
80. 🟡 Why can't you put a CNAME at the root (apex) domain? What are ALIAS/ANAME records?
81. 🟡 What is TTL in DNS? How does it affect migrations?
82. 🟡 What is a recursive query vs an iterative query?
83. 🟡 What is reverse DNS (PTR)?
84. 🟡 What is `/etc/hosts` and `/etc/resolv.conf`? What is the order of name resolution (`/etc/nsswitch.conf`)?
85. 🟡 Does DNS use TCP or UDP? When does it use TCP?
86. 🟡 What is split-horizon DNS?
87. 🟡 What is DNS caching and where does it happen (browser, OS, resolver)?
88. 🟡 What is DNS-based load balancing and GeoDNS?
89. 🔴 What are DNS spoofing/cache poisoning and DNSSEC?
90. 🔴 What are DNS over HTTPS (DoH) and DNS over TLS (DoT)?
91. 🔴 Why can a .NET or Java application keep connecting to an old IP after a DNS change?

---

## 9. DHCP, ARP & ICMP

92. 🟢 What is DHCP? Explain the DORA process.
93. 🟡 What is a DHCP lease? What is a DHCP reservation?
94. 🟢 What is ARP? How does it map IP to MAC?
95. 🟡 What is ARP spoofing/poisoning?
96. 🟢 What is ICMP? Which tools use it (ping, traceroute)?
97. 🟡 Why might ping fail even though the server is up?
98. 🟡 How does traceroute work (TTL expiry)?

---

## 10. Switching, Routing, VLANs & NAT

99. 🟢 What is switching? How does a switch learn MAC addresses?
100. 🟢 What is routing? What is a routing table?
101. 🟡 What is static routing vs dynamic routing?
102. 🟡 What are routing protocols (RIP, OSPF, EIGRP, BGP) at a high level?
103. 🟡 What is BGP and why does it matter for the internet?
104. 🟡 What is a VLAN? Why use VLANs?
105. 🟡 What is trunking (802.1Q)?
106. 🟢 What is NAT? Why is it needed?
107. 🟡 What are SNAT, DNAT and PAT (port address translation)?
108. 🟡 What is port forwarding?
109. 🟡 What is a NAT gateway in the cloud?
110. 🔴 What is SNAT port exhaustion and how can it affect outbound API calls from many app servers?

---

## 11. HTTP, HTTPS & TLS

111. 🟢 What is HTTP? What are its methods and status code classes?
112. 🟢 What is HTTPS? How is it different from HTTP?
113. 🟢 What is TLS? What is the difference between SSL and TLS?
114. 🟡 Explain the TLS handshake (ClientHello, ServerHello, certificate, key exchange, finished).
115. 🟡 What changed in TLS 1.3 vs TLS 1.2?
116. 🟡 What is a digital certificate? What does it contain?
117. 🟡 What is a Certificate Authority (CA)? What is the chain of trust (root, intermediate, leaf)?
118. 🟡 What is a self-signed certificate? When is it acceptable?
119. 🟡 What is symmetric vs asymmetric encryption? Where is each used in TLS?
120. 🟡 What is SNI (Server Name Indication)?
121. 🟡 What is mTLS (mutual TLS)? 💰
122. 🟡 What is HSTS?
123. 🟡 What is certificate pinning?
124. 🟡 What are certificate formats (PEM, DER, PFX/PKCS#12, CRT, KEY)?
125. 🟡 What are CSR, OCSP and CRL?
126. 🟡 What is Let's Encrypt and ACME?
127. 🔴 What happens when a certificate expires in production? How do you prevent it? 💰
128. 🔴 Why do you get "certificate verify failed" / "unable to get local issuer certificate" errors?
129. 🟡 What are HTTP/1.1, HTTP/2 and HTTP/3 differences?
130. 🟡 What are cookies, sessions and CORS from a network perspective?

---

## 12. Proxies, Load Balancers & CDNs

131. 🟢 What is a proxy server? Forward proxy vs reverse proxy?
132. 🟢 What is a load balancer? Layer 4 vs Layer 7?
133. 🟡 What load balancing algorithms exist?
134. 🟡 What are health checks?
135. 🟡 What are sticky sessions?
136. 🟡 What headers do proxies add (`X-Forwarded-For`, `X-Forwarded-Proto`, `X-Real-IP`, `Forwarded`)?
137. 🟡 What is SSL termination, SSL passthrough and SSL re-encryption?
138. 🟡 What is a CDN? How does it work?
139. 🟡 What is a transparent proxy?
140. 🔴 How do corporate proxies affect applications calling external APIs (`HTTP_PROXY`, `HTTPS_PROXY`, `NO_PROXY`)?

---

## 13. Firewalls, VPNs & Network Security

141. 🟢 What is a firewall? What types exist (packet filtering, stateful, application/next-gen, WAF)?
142. 🟡 What is a stateful vs stateless firewall?
143. 🟡 What is a DMZ?
144. 🟢 What is a VPN? What are site-to-site and remote-access VPNs?
145. 🟡 What are IPsec, OpenVPN and WireGuard?
146. 🟡 What is an IDS vs an IPS?
147. 🟡 What is a WAF?
148. 🟡 What are common network attacks (DDoS, MITM, spoofing, sniffing, port scanning)?
149. 🟡 What is a DDoS attack? How is it mitigated?
150. 🟡 What is network segmentation? 💰
151. 🟡 What is zero trust networking?
152. 🔴 What is a bastion host / jump server? 💰
153. 🔴 How do banks typically segment networks (internet zone, DMZ, application zone, database zone)? 💰

---

## 14. Cloud Networking

154. 🟢 What is a VPC (Virtual Private Cloud) / VNet?
155. 🟡 What are public and private subnets?
156. 🟡 What is an internet gateway vs a NAT gateway?
157. 🟡 What are route tables?
158. 🟡 What are security groups vs network ACLs?
159. 🟡 What is VPC peering and a transit gateway?
160. 🟡 What is a private endpoint / PrivateLink?
161. 🟡 What is Direct Connect / ExpressRoute? 💰
162. 🟡 What is an elastic/static public IP?
163. 🔴 How would you design networking for a three-tier app (web, app, DB) in the cloud?

---

## 15. Container & Kubernetes Networking

164. 🟡 How does Docker networking work (bridge, host, none, overlay)?
165. 🟡 What does `-p 8080:80` do in Docker?
166. 🟡 How do containers resolve each other's names in Docker Compose?
167. 🟡 How does Kubernetes networking work (every pod gets an IP)?
168. 🟡 What are ClusterIP, NodePort, LoadBalancer and Ingress?
169. 🟡 What is CoreDNS in Kubernetes?
170. 🟡 What are CNI plugins (Calico, Flannel, Cilium, OVN-Kubernetes in OpenShift)?
171. 🟡 What are Network Policies in Kubernetes?
172. 🟡 What is a service mesh and how does it handle networking (sidecars, mTLS)?
173. 🔴 What is OpenShift and how does its networking (Routes, OVN-Kubernetes) differ from plain Kubernetes?

---

## 16. Network Troubleshooting Tools

174. 🟢 What does `ping` do? What does it tell you?
175. 🟢 What does `traceroute` / `tracepath` / `mtr` do?
176. 🟢 What do `nslookup`, `dig` and `host` do? How are they different?
177. 🟡 What does `curl -v` show? How do you test an HTTPS endpoint with headers and timing (`curl -w`)?
178. 🟡 What do `ss` and `netstat` show? Which flags do you use (`ss -tulnp`)?
179. 🟡 What does `telnet host port` or `nc -zv host port` test?
180. 🟡 What does `tcpdump` do? How do you capture traffic on port 443?
181. 🟡 What is Wireshark?
182. 🟡 What does `openssl s_client -connect host:443` show?
183. 🟡 What do `ip addr`, `ip route` and `ip neigh` show?
184. 🟡 What does `arp -a` show?
185. 🟡 How do you check which process is listening on a port (`ss -tulnp`, `lsof -i :8080`)?
186. 🔴 What is your step-by-step approach when "the application cannot connect to the database"?
187. 🔴 What is your step-by-step approach when "the website is slow for some users only"?

---

# Part B — Red Hat Enterprise Linux

## 17. Linux & RHEL Fundamentals

188. 🟢 What is Linux? What is a Linux distribution?
189. 🟢 What is the Linux kernel? What is the shell?
190. 🟢 What is Red Hat Enterprise Linux (RHEL)? Why is it popular in enterprises and banks?
191. 🟡 What is the difference between RHEL, Fedora, CentOS Stream, Rocky Linux, AlmaLinux and Oracle Linux?
192. 🟡 What happened to CentOS Linux, and what is CentOS Stream?
193. 🟡 What are the RHEL release versions (7, 8, 9, 10) and support lifecycle?
194. 🟡 What is a Red Hat subscription? What is `subscription-manager`?
195. 🟡 What are RHCSA and RHCE certifications?
196. 🟢 What is the difference between Linux and Windows server administration?
197. 🟢 What are common shells (bash, sh, zsh)? What is the default shell in RHEL?
198. 🟢 What is the root user? Why shouldn't you log in as root?
199. 🟡 What is a kernel module? How do you list and load modules (`lsmod`, `modprobe`)?
200. 🟡 How do you check the OS version and kernel version (`cat /etc/redhat-release`, `cat /etc/os-release`, `uname -r`, `hostnamectl`)?

---

## 18. File System Hierarchy & Basic Commands

201. 🟢 Explain the Linux filesystem hierarchy (`/`, `/etc`, `/var`, `/usr`, `/home`, `/opt`, `/tmp`, `/boot`, `/dev`, `/proc`, `/sys`, `/run`, `/root`).
202. 🟢 What is stored in `/etc`? In `/var/log`? In `/opt`?
203. 🟢 What is `/proc`? What is `/sys`?
204. 🟢 What is the difference between absolute and relative paths?
205. 🟢 What do `pwd`, `cd`, `ls -la`, `mkdir -p`, `rmdir`, `rm -rf`, `cp -r`, `mv`, `touch` do?
206. 🟢 What do `cat`, `less`, `more`, `head`, `tail`, `tail -f` do?
207. 🟢 What is the difference between a hard link and a soft (symbolic) link? (`ln`, `ln -s`)
208. 🟡 What is an inode? What happens when you run out of inodes?
209. 🟡 What do `df -h` and `du -sh` show? What's the difference?
210. 🟡 What does `file`, `stat` and `which`/`whereis`/`type` do?
211. 🟡 How do you archive and compress files (`tar -czvf`, `tar -xzvf`, `gzip`, `zip`, `xz`)?
212. 🟡 What are stdin, stdout and stderr? What do `>`, `>>`, `2>`, `2>&1`, `&>` and `|` do?
213. 🟡 What is `/dev/null`?
214. 🟡 How do you find files (`find / -name "*.log" -mtime +7 -size +100M`)?
215. 🟡 What is `locate` vs `find`?
216. 🟡 What does `tee` do?
217. 🟡 What are environment variables? How do you view and set them (`env`, `export`, `echo $PATH`)?
218. 🟡 What are `.bashrc`, `.bash_profile` and `/etc/profile`? When is each loaded?
219. 🟡 What is `alias`?

---

## 19. Text Processing & Searching

220. 🟢 What does `grep` do? What are common flags (`-i`, `-r`, `-n`, `-v`, `-c`, `-E`, `-A`, `-B`)?
221. 🟡 What does `awk` do? Print the 1st and 3rd columns of a file.
222. 🟡 What does `sed` do? Replace a string in a file in place.
223. 🟡 What do `cut`, `sort`, `uniq`, `wc`, `tr` do?
224. 🟡 How do you find the top 10 IP addresses in an Nginx access log?
225. 🟡 How do you count the number of 500 errors in a log file?
226. 🟡 How do you search for a string in all files under a directory recursively?
227. 🟡 What is `xargs`?
228. 🟡 What is `diff`?
229. 🟡 What are regular expressions? Basic vs extended regex?
230. 🟡 What is `vi`/`vim`? How do you edit, save, quit, search and replace in vim?
231. 🟡 What is `nano`?
232. 🟡 How do you view a JSON log nicely (`jq`)?

---

## 20. File Permissions, Ownership, ACLs & Special Permissions

233. 🟢 What do Linux file permissions `rwx` mean for files and directories?
234. 🟢 What are owner, group and others?
235. 🟢 What does `chmod 755`, `chmod 644`, `chmod 600` mean?
236. 🟢 What does `chmod u+x`, `g-w`, `o=r` mean?
237. 🟢 What does `chown user:group file` do? What does `chgrp` do?
238. 🟡 What is umask? How is the default permission calculated?
239. 🟡 What are SUID, SGID and the sticky bit? Give examples (`/usr/bin/passwd`, `/tmp`).
240. 🟡 What does `chmod 4755`, `2755`, `1777` mean?
241. 🟡 What are ACLs? How do you use `getfacl` and `setfacl`?
242. 🟡 What does the `+` at the end of `ls -l` permissions mean?
243. 🟡 What are file attributes (`chattr +i`, `lsattr`)?
244. 🔴 Why does "Permission denied" happen even when `chmod 777` is set? (SELinux, ACLs, parent directory permissions, mount options like `noexec`)

---

## 21. Users, Groups & sudo

245. 🟢 How do you create, modify and delete users (`useradd`, `usermod`, `userdel`)?
246. 🟢 How do you set or change a password (`passwd`)?
247. 🟢 What are `/etc/passwd`, `/etc/shadow` and `/etc/group`?
248. 🟡 What is the difference between primary and secondary groups?
249. 🟡 How do you add a user to a group (`usermod -aG`)? Why is `-a` important?
250. 🟡 What is a system user vs a regular user? How do you create a service account with no login shell?
251. 🟡 What is password aging (`chage`)?
252. 🟡 What is `sudo`? How do you configure it (`visudo`, `/etc/sudoers.d/`)?
253. 🟡 What is the `wheel` group in RHEL?
254. 🟡 What is `su` vs `sudo` vs `sudo -i`?
255. 🟡 How do you lock and unlock a user account?
256. 🟡 How do you see who is logged in (`who`, `w`, `last`, `id`, `whoami`)?
257. 🔴 How do you integrate RHEL with Active Directory / LDAP (SSSD, realmd, IdM/FreeIPA)? 💰

---

## 22. Processes, Jobs & Signals

258. 🟢 What is a process? What is a PID? What is PID 1 in RHEL?
259. 🟢 What do `ps aux`, `ps -ef`, `top`, `htop` show?
260. 🟢 How do you find a process by name (`pgrep`, `ps aux | grep`)?
261. 🟢 How do you kill a process (`kill`, `kill -9`, `pkill`, `killall`)?
262. 🟡 What are signals? What are SIGTERM (15), SIGKILL (9), SIGHUP (1), SIGINT (2), SIGSTOP, SIGCONT?
263. 🟡 Why should you prefer SIGTERM over SIGKILL?
264. 🟡 What is a zombie process? What is an orphan process?
265. 🟡 What are process states (R, S, D, Z, T)? What does the D state mean?
266. 🟡 What are foreground and background jobs (`&`, `jobs`, `fg`, `bg`, `Ctrl+Z`)?
267. 🟡 What is `nohup`? What are `screen` and `tmux`?
268. 🟡 What are `nice` and `renice`?
269. 🟡 What is load average? How do you interpret it relative to CPU cores?
270. 🟡 What is a daemon?
271. 🔴 What is `/proc/<pid>/`? What useful information can you find there (fd, status, limits, environ)?
272. 🔴 What are ulimits (`ulimit -n`, `/etc/security/limits.conf`) and why do they matter for web servers ("too many open files")?

---

## 23. systemd, Services & Targets

273. 🟢 What is systemd? What did it replace (SysV init)?
274. 🟢 How do you start, stop, restart, reload and check the status of a service (`systemctl`)?
275. 🟢 What is the difference between `systemctl enable` and `systemctl start`? What does `enable --now` do?
276. 🟡 What is a unit file? Where are unit files stored (`/usr/lib/systemd/system`, `/etc/systemd/system`)?
277. 🟡 What are unit types (service, socket, timer, target, mount, path)?
278. 🟡 What are the main sections of a service unit file (`[Unit]`, `[Service]`, `[Install]`)?
279. 🟡 What do `ExecStart`, `Restart=always`, `RestartSec`, `User`, `WorkingDirectory`, `Environment`, `EnvironmentFile`, `After`, `Wants`, `Requires` mean?
280. 🟡 What is `systemctl daemon-reload` and when must you run it?
281. 🟡 What are service types (`simple`, `exec`, `forking`, `oneshot`, `notify`)?
282. 🟡 What are targets? What are `multi-user.target` and `graphical.target`? How do you change the default target?
283. 🟡 What is `systemctl mask` vs `disable`?
284. 🟡 How do you see why a service failed (`systemctl status`, `journalctl -u service -xe`)?
285. 🟡 How do you override a vendor unit file safely (`systemctl edit`, drop-in files)?
286. 🟡 How do you list failed services (`systemctl --failed`)?
287. 🔴 How do you configure graceful shutdown for an app via systemd (`KillSignal`, `TimeoutStopSec`)?
288. 🔴 What are systemd resource controls (`MemoryMax`, `CPUQuota`) and cgroups?
289. 🔴 How do you analyse slow boot (`systemd-analyze blame`)?

---

## 24. Package Management (dnf, yum, rpm, repositories, subscription)

290. 🟢 What is RPM? What is a `.rpm` package?
291. 🟢 What is `dnf`? What is `yum`? How are they related in RHEL 8/9?
292. 🟢 How do you install, remove, update and search for packages (`dnf install`, `remove`, `update`, `search`, `info`)?
293. 🟡 How do you list installed packages and find which package provides a file (`rpm -qa`, `rpm -qf`, `dnf provides`)?
294. 🟡 What is a repository? Where are repo files stored (`/etc/yum.repos.d/`)?
295. 🟡 What are BaseOS and AppStream repositories in RHEL 8/9?
296. 🟡 What are module streams (`dnf module list`)? (Note: deprecated/less used in RHEL 10.)
297. 🟡 What is EPEL?
298. 🟡 How do you install a local `.rpm` file with dependencies?
299. 🟡 How do you roll back an update (`dnf history`, `dnf history undo`)?
300. 🟡 How do you apply only security updates (`dnf update --security`)? 💰
301. 🟡 How do you register a system and attach repositories (`subscription-manager register`, `repos --enable`)?
302. 🔴 How do you set up a local/offline repository for servers without internet access (common in banks)? 💰
303. 🔴 What is Red Hat Satellite?

---

## 25. Storage — Disks, Partitions, Filesystems, Mounts, fstab

304. 🟢 How do you list disks and partitions (`lsblk`, `fdisk -l`, `blkid`)?
305. 🟡 What is MBR vs GPT?
306. 🟡 How do you create a partition (`fdisk`, `gdisk`, `parted`)?
307. 🟡 What filesystems are supported in RHEL (XFS default, ext4, vfat)? Why is XFS the default?
308. 🟡 How do you create a filesystem (`mkfs.xfs`, `mkfs.ext4`)?
309. 🟡 How do you mount and unmount (`mount`, `umount`)?
310. 🟡 What is `/etc/fstab`? What are its fields? Why use UUIDs instead of `/dev/sdb1`?
311. 🟡 What happens if `/etc/fstab` has a wrong entry? How do you recover?
312. 🟡 What is swap? How do you create and enable a swap file/partition?
313. 🟡 Can an XFS filesystem be shrunk?
314. 🟡 How do you grow an XFS filesystem (`xfs_growfs`) and an ext4 filesystem (`resize2fs`)?
315. 🟡 What is NFS? How do you mount an NFS share?
316. 🟡 What is autofs?
317. 🟡 What is SMB/CIFS mounting?
318. 🔴 What is "device is busy" when unmounting, and how do you find the process (`lsof`, `fuser`)?
319. 🔴 Why does `df` show a full disk while `du` doesn't (deleted files held open by a process)?

---

## 26. LVM & Stratis

320. 🟡 What is LVM? Why use it?
321. 🟡 What are PV (physical volume), VG (volume group) and LV (logical volume)?
322. 🟡 How do you create PVs, VGs and LVs (`pvcreate`, `vgcreate`, `lvcreate`)?
323. 🟡 How do you extend a logical volume and its filesystem (`lvextend -r`)?
324. 🟡 How do you add a new disk to an existing volume group (`vgextend`)?
325. 🟡 What are LVM snapshots?
326. 🟡 How do you view LVM details (`pvs`, `vgs`, `lvs`, `pvdisplay`, `vgdisplay`, `lvdisplay`)?
327. 🟡 What is Stratis in RHEL?
328. 🟡 What is VDO (deduplication and compression)?
329. 🔴 How do you extend the root filesystem on a running RHEL server without downtime?

---

## 27. Networking on RHEL (NetworkManager, nmcli, ip, ss)

330. 🟢 How do you see the IP address of a RHEL server (`ip a`, `hostname -I`)?
331. 🟡 What is NetworkManager? What is `nmcli`? What is `nmtui`?
332. 🟡 How do you configure a static IP using `nmcli`?
333. 🟡 Where are network connection profiles stored in RHEL 9 (keyfiles in `/etc/NetworkManager/system-connections/`) vs older `ifcfg` files?
334. 🟡 How do you set DNS servers and the hostname (`nmcli`, `hostnamectl set-hostname`)?
335. 🟡 How do you add a static route?
336. 🟡 What is network bonding/teaming? (Note: teaming deprecated in RHEL 9.)
337. 🟡 How do you check open ports and listening services (`ss -tulnp`)?
338. 🟡 How do you test connectivity to a remote port from RHEL (`curl`, `nc`, `timeout 3 bash -c '</dev/tcp/host/port'`)?
339. 🟡 How do you change kernel network parameters (`sysctl`, `/etc/sysctl.d/`) — e.g., `net.ipv4.ip_forward`, `net.core.somaxconn`?
340. 🔴 How do you tune Linux networking for a high-traffic web server (somaxconn, tcp_tw_reuse, ip_local_port_range, file descriptors)?

---

## 28. firewalld

341. 🟢 What is firewalld? How is it related to nftables/iptables?
342. 🟢 How do you check firewalld status and the active zones (`firewall-cmd --state`, `--get-active-zones`)?
343. 🟡 What are zones (public, internal, trusted, dmz, drop, block)?
344. 🟡 How do you open a port permanently (`firewall-cmd --permanent --add-port=8080/tcp` then `--reload`)?
345. 🟡 How do you allow a service (`--add-service=http`)?
346. 🟡 What is the difference between runtime and permanent configuration?
347. 🟡 How do you list all rules (`--list-all`)?
348. 🟡 How do you allow traffic only from a specific IP (rich rules or sources)?
349. 🟡 How do you set up port forwarding with firewalld?
350. 🔴 Your app works on `localhost` but not from another machine. How do you check whether firewalld is the cause?

---

## 29. SELinux

351. 🟢 What is SELinux? Why does RHEL enable it by default?
352. 🟢 What are SELinux modes (enforcing, permissive, disabled)? How do you check them (`getenforce`, `sestatus`)?
353. 🟡 How do you change the mode temporarily (`setenforce 0/1`) and permanently (`/etc/selinux/config`)?
354. 🟡 Why should you NOT disable SELinux in production? 💰
355. 🟡 What is an SELinux context/label (user:role:type:level)? How do you view it (`ls -Z`, `ps -Z`)?
356. 🟡 What is type enforcement?
357. 🟡 What are SELinux booleans? How do you list and set them (`getsebool -a`, `setsebool -P`)?
358. 🟡 What is `httpd_can_network_connect` and why is it needed when Nginx proxies to a backend app?
359. 🟡 How do you allow Nginx to listen on a non-standard port (`semanage port -a -t http_port_t -p tcp 8081`)?
360. 🟡 How do you fix file contexts (`restorecon -Rv`, `semanage fcontext -a -t httpd_sys_content_t "/data/www(/.*)?"`)?
361. 🟡 What is the difference between `chcon` and `semanage fcontext` + `restorecon`?
362. 🟡 How do you find SELinux denials (`/var/log/audit/audit.log`, `ausearch -m avc`, `sealert`, `journalctl`)?
363. 🟡 What is `audit2allow` and when should you (not) use it?
364. 🔴 Your app works with `setenforce 0` but fails in enforcing mode. How do you troubleshoot properly?
365. 🔴 Why can a file moved with `mv` keep the wrong SELinux context, while `cp` gets the right one?

---

## 30. SSH & Remote Access

366. 🟢 What is SSH? How does it work?
367. 🟢 How do you connect to a server using SSH with a username and key?
368. 🟡 How do you generate SSH keys (`ssh-keygen`) and copy them (`ssh-copy-id`)?
369. 🟡 What are `~/.ssh/authorized_keys`, `known_hosts` and `~/.ssh/config`?
370. 🟡 What permissions must `~/.ssh` and `authorized_keys` have?
371. 🟡 How do you harden SSH (`/etc/ssh/sshd_config`: disable root login, disable password auth, change port, `AllowUsers`)? 💰
372. 🟡 How do you copy files securely (`scp`, `rsync`, `sftp`)?
373. 🟡 What is SSH port forwarding (local `-L`, remote `-R`, dynamic `-D`)?
374. 🟡 What is a jump host / bastion (`ssh -J`)?
375. 🟡 What is `ssh-agent`?
376. 🔴 Why do you get "Permission denied (publickey)" and how do you debug it (`ssh -vvv`)?
377. 🔴 How do you change the SSH port when SELinux and firewalld are enabled?

---

## 31. Logging — journald, rsyslog, logrotate

378. 🟢 Where are logs stored in RHEL (`/var/log/messages`, `/var/log/secure`, `/var/log/audit/audit.log`, `/var/log/nginx/`)?
379. 🟢 What is `journalctl`? How do you view logs of a service (`journalctl -u nginx`)?
380. 🟡 How do you follow logs (`journalctl -f`), filter by time (`--since "1 hour ago"`), by priority (`-p err`) and by boot (`-b`)?
381. 🟡 How do you make the journal persistent across reboots (`/var/log/journal`)?
382. 🟡 What is rsyslog? How do you forward logs to a central server?
383. 🟡 What is logrotate? How do you configure log rotation for an application?
384. 🟡 What is `dmesg`?
385. 🟡 Where are failed login attempts recorded? How do you view them (`lastb`, `/var/log/secure`, `journalctl _COMM=sshd`)?
386. 🔴 Your disk filled up because of logs. How do you find and fix it permanently?

---

## 32. Scheduling — cron, at, systemd timers

387. 🟢 What is cron? How do you edit and list a user's crontab (`crontab -e`, `crontab -l`)?
388. 🟢 Explain the cron syntax (`* * * * *`). Write cron entries for: every 5 minutes, daily at 2:30 AM, every Monday at 9 AM, the 1st of every month.
389. 🟡 Where are system cron jobs stored (`/etc/crontab`, `/etc/cron.d/`, `/etc/cron.daily/`)?
390. 🟡 Why does a script work manually but fail in cron (environment variables, PATH, working directory)?
391. 🟡 How do you log cron job output?
392. 🟡 What is `at` and `atq`?
393. 🟡 What are systemd timers? How are they better than cron?
394. 🟡 What is anacron?
395. 🔴 How do you prevent a cron job from running twice at the same time (`flock`)?

---

## 33. Shell Scripting (Bash)

396. 🟢 What is a shell script? What is the shebang (`#!/bin/bash`)?
397. 🟢 How do you make a script executable and run it?
398. 🟢 How do you declare variables and read user input?
399. 🟡 What are `$0`, `$1`, `$#`, `$@`, `$*`, `$?`, `$$`?
400. 🟡 How do you write `if`, `for`, `while` and `case` statements?
401. 🟡 What are exit codes? How do you check whether a command succeeded?
402. 🟡 What do `set -e`, `set -u`, `set -o pipefail` and `set -x` do?
403. 🟡 What is the difference between single quotes, double quotes and backticks / `$(...)`?
404. 🟡 How do you write functions in bash?
405. 🟡 How do you read a file line by line?
406. 🟡 What is `[ ]` vs `[[ ]]`?
407. 🟡 How do you check whether a file or directory exists?
408. 🟡 What is a here document (`<<EOF`)?
409. 🔴 Write a script that checks if a service is running and restarts it if not.
410. 🔴 Write a script that deletes log files older than 7 days and compresses files older than 1 day.
411. 🔴 Write a script that checks disk usage and sends an alert if usage > 80%.
412. 🔴 Write a script that checks whether a list of URLs return HTTP 200.
413. 🔴 Write a script that takes a database backup and keeps only the last 7 backups.

---

## 34. Performance Monitoring & Troubleshooting

414. 🟢 How do you check CPU usage (`top`, `htop`, `mpstat`)?
415. 🟢 How do you check memory usage (`free -h`, `/proc/meminfo`)?
416. 🟡 What do "used", "free", "buff/cache" and "available" mean in `free -h`?
417. 🟡 What is the OOM killer? How do you find out if it killed your process (`dmesg`, `journalctl -k`)?
418. 🟡 How do you check disk I/O (`iostat`, `iotop`)?
419. 🟡 What does `vmstat` show?
420. 🟡 What does `sar` show? How do you see historical performance data?
421. 🟡 What is iowait? What does high iowait indicate?
422. 🟡 How do you find which process is using the most CPU or memory?
423. 🟡 How do you check open file descriptors for a process (`lsof -p`, `ls /proc/<pid>/fd | wc -l`)?
424. 🟡 What is `strace`? When would you use it?
425. 🟡 What is `uptime` and load average?
426. 🟡 What is tuned / tuned profiles in RHEL?
427. 🔴 What is your step-by-step approach when a RHEL server is slow?
428. 🔴 How do you diagnose a memory leak in an application running on Linux?
429. 🔴 How do you capture a dump of a .NET process on Linux (`dotnet-dump`, `createdump`)?

---

## 35. Boot Process, GRUB & Recovery

430. 🟡 Explain the RHEL boot process (BIOS/UEFI → GRUB2 → kernel → initramfs → systemd → targets).
431. 🟡 What is GRUB2? Where is its configuration (`/etc/default/grub`, `grub2-mkconfig`)?
432. 🟡 What is `grubby`?
433. 🟡 What is initramfs? How do you rebuild it (`dracut`)?
434. 🟡 How do you boot into rescue or emergency mode?
435. 🟡 How do you reset a forgotten root password on RHEL 8/9 (`rd.break`, `chroot /sysroot`, `touch /.autorelabel`)?
436. 🟡 Why is `/.autorelabel` needed after resetting the root password?
437. 🔴 The server doesn't boot after editing `/etc/fstab`. How do you fix it?
438. 🔴 How do you boot an older kernel after a kernel update breaks something?

---

## 36. Security Hardening & Compliance

439. 🟡 What are the basic steps to harden a RHEL server? 💰
440. 🟡 How do you disable unnecessary services?
441. 🟡 How do you enforce password policies (`/etc/security/pwquality.conf`, `faillock`)?
442. 🟡 What is `faillock` and how do you unlock a locked user?
443. 🟡 What is auditd? How do you add audit rules (`auditctl`, `/etc/audit/rules.d/`)? 💰
444. 🟡 What are crypto policies in RHEL (`update-crypto-policies`, DEFAULT, FUTURE, FIPS)?
445. 🟡 What is FIPS mode and why do banks require it? 💰
446. 🟡 What is OpenSCAP? How do you scan a system against CIS or PCI-DSS profiles? 💰
447. 🟡 What is AIDE (file integrity monitoring)? 💰
448. 🟡 How do you keep servers patched with minimal downtime?
449. 🟡 What is `fapolicyd`?
450. 🔴 How do you audit who ran `sudo` commands and what they ran? 💰

---

## 37. Containers on RHEL — Podman, Buildah, Skopeo

451. 🟡 What is Podman? How is it different from Docker (daemonless, rootless)?
452. 🟡 What are Buildah and Skopeo?
453. 🟡 What are UBI (Universal Base Images)? Why use them?
454. 🟡 How do you run, list, stop and remove containers with Podman?
455. 🟡 What is rootless Podman? What are its limitations (ports below 1024)?
456. 🟡 What are Podman pods?
457. 🟡 How do you run a Podman container as a systemd service (Quadlet / `podman generate systemd`)?
458. 🟡 Why do you need the `:Z` or `:z` suffix on volume mounts with SELinux?
459. 🟡 Is `docker` command available on RHEL? What is `podman-docker`?
460. 🔴 How do you run a .NET application container from the Red Hat .NET UBI images?

---

## 38. Hosting .NET & Nginx on RHEL

461. 🟢 How do you install the .NET SDK/runtime on RHEL (`dnf install dotnet-sdk-8.0` / `aspnetcore-runtime-8.0`)?
462. 🟢 How do you install Nginx on RHEL and enable it to start at boot?
463. 🟡 How do you publish an ASP.NET Core app and copy it to a RHEL server?
464. 🟡 How do you create a systemd service file for an ASP.NET Core app (User, WorkingDirectory, ExecStart, Restart, Environment, KillSignal)?
465. 🟡 Which user should the app run as? How do you create a dedicated service account?
466. 🟡 How do you configure Nginx as a reverse proxy to Kestrel on RHEL?
467. 🟡 Why does Nginx return 502 Bad Gateway on RHEL even though the app is running? (SELinux `httpd_can_network_connect`)
468. 🟡 What SELinux booleans and port labels are needed for Nginx to proxy to `localhost:5000`?
469. 🟡 Which firewalld rules are needed for HTTP/HTTPS?
470. 🟡 Where are Nginx configuration files on RHEL (`/etc/nginx/nginx.conf`, `/etc/nginx/conf.d/`) and how do you test them (`nginx -t`)?
471. 🟡 How do you view logs for the .NET app and for Nginx on RHEL?
472. 🟡 How do you set environment variables (e.g., `ASPNETCORE_ENVIRONMENT`, connection strings) securely for a systemd service?
473. 🟡 How do you install TLS certificates for Nginx on RHEL and fix SELinux contexts for certificate files?
474. 🟡 How do you serve static files from a custom directory with correct SELinux labels?
475. 🟡 How do you deploy a new version of the app with minimal downtime on a single RHEL server?
476. 🟡 How do you configure log rotation for the app logs?
477. 🔴 How do you trust an internal corporate CA certificate on RHEL so that .NET `HttpClient` can call internal HTTPS APIs (`update-ca-trust`)? 💰
478. 🔴 How do you configure the app to use a corporate proxy for outbound calls on RHEL?
479. 🔴 How do you increase file descriptor limits for Nginx and the .NET service?
480. 🔴 How do you diagnose high CPU in a .NET process on RHEL (`top -H`, `dotnet-counters`, `dotnet-trace`)?

---

# Part C — Practice

## 39. Financial-Domain Questions 💰

481. 🟡💰 Why do banks prefer RHEL for production servers?
482. 🟡💰 Why is time synchronisation (chrony/NTP) critical for financial transactions and logs?
483. 🟡💰 How do you configure chrony on RHEL and verify sync (`chronyc tracking`, `chronyc sources`)?
484. 🔴💰 How are servers typically segmented in a bank's network (DMZ, app, DB, management zones)?
485. 🔴💰 How do you allow an application server to reach only the database server and nothing else?
486. 🔴💰 How do you secure communication with partner banks (mTLS, IP whitelisting, VPN/leased line)?
487. 🔴💰 How do you meet audit requirements on Linux servers (auditd, sudo logs, central logging, retention)?
488. 🔴💰 How do you patch production servers in a bank with change management and rollback?
489. 🔴💰 How do you handle certificate renewals for dozens of internal services without outages?
490. 🔴💰 How do you run applications on servers with no internet access (offline repos, internal registries, internal NuGet feeds)?

---

## 40. Tricky Questions

491. 🟡 Why does `ping` work but `curl` to the same server fails?
492. 🟡 Why does `curl` work but the browser shows a certificate error?
493. 🟡 Why does an app work on `localhost:5000` but not on `server-ip:5000`? (binding to 127.0.0.1, firewalld)
494. 🟡 What is the difference between binding to `127.0.0.1` and `0.0.0.0`?
495. 🟡 Why can a DNS change take hours to reflect for some users?
496. 🟡 Why can there be many TIME_WAIT connections on a busy server, and is it a problem?
497. 🟡 Why does `rm` of a large log file not free disk space?
498. 🟡 Why does `chmod 777` not fix "Permission denied" on RHEL?
499. 🟡 Why does Nginx return 403 Forbidden for files that clearly exist?
500. 🟡 Why does Nginx return 502 only on RHEL but works on Ubuntu with the same config?
501. 🟡 Why does a service start manually but fail when started by systemd?
502. 🟡 Why does a cron job not run even though the syntax looks correct?
503. 🟡 Why does `sudo` say "user is not in the sudoers file"?
504. 🟡 Why does SSH key login still ask for a password?
505. 🟡 Why can't a non-root process listen on port 80?
506. 🟡 Why does `df -h` show 100% but you can't find big files?
507. 🟡 Why does `free -h` show very little free memory even though the server is idle?
508. 🟡 Why is `kill -9` not always the right way to stop a process?
509. 🟡 Why does a firewalld rule stop working after a reboot?
510. 🟡 Why does `setenforce 0` fix the issue, and why is that not the solution?
511. 🟡 Can two processes listen on the same port? When (SO_REUSEPORT)?
512. 🟡 Why do outbound connections fail with "Cannot assign requested address" under heavy load?
513. 🔴 Why does a TCP connection hang instead of failing immediately when a firewall drops packets?
514. 🔴 Why can a large MTU cause some HTTPS requests to hang (MTU/PMTUD issues)?
515. 🔴 Why does an application see connection resets when talking through a load balancer after idle periods?

---

## 41. Predict the Output (Commands & Configs)

> What does each command or configuration do or output? If it's wrong, explain why.

516. 🟢 `ls -l file.txt` shows `-rw-r-----`. Who can read, write and execute it?
517. 🟢 `chmod 640 secret.conf` — what are the resulting permissions?
518. 🟡 `umask 027` — what are the default permissions of a new file and a new directory?
519. 🟡 `echo "hello" > file; echo "world" >> file; cat file` — what is printed?
520. 🟡 `command > out.log 2>&1` vs `command 2>&1 > out.log` — what's the difference?
521. 🟡 `grep -c "ERROR" app.log | wc -l` — what does this print and why is it probably wrong?
522. 🟡 `awk '{print $1}' access.log | sort | uniq -c | sort -nr | head -5` — what does this output?
523. 🟡 `find /var/log -name "*.log" -mtime +30 -delete` — what does it do?
524. 🟡 `tar -czvf backup.tar.gz /etc/nginx` — what does it create?
525. 🟡 `ss -tulnp | grep :443` — what information does it show?
526. 🟡 `systemctl enable nginx` — does Nginx start now?
527. 🟡 `firewall-cmd --add-port=8080/tcp` (without `--permanent`) — what happens after a reboot?
528. 🟡 `setsebool httpd_can_network_connect on` (without `-P`) — what happens after a reboot?
529. 🟡 `kill -15 1234` vs `kill -9 1234` — what's the difference in behaviour?
530. 🟡 `*/15 2-4 * * 1-5 /opt/scripts/sync.sh` — when does it run?
531. 🟡 `ln -s /opt/app/v2 /opt/app/current` — what is created? What happens if v2 is deleted?
532. 🟡 `curl -I https://example.com` — what is shown?
533. 🟡 `dig +short example.com` vs `nslookup example.com` — what's the difference in output?
534. 🟡 `ip route` shows `default via 10.0.0.1 dev eth0` — what does it mean?
535. 🟡 A subnet is `10.10.0.0/22`. What are the first and last usable IPs and how many hosts?
536. 🟡 `set -e` is at the top of a script, and a `grep` command finds no match. What happens?
537. 🟡 `ls -Z /var/www/html/index.html` shows `user_home_t`. What problem will Nginx have?
538. 🟡 `/etc/fstab` entry: `UUID=xxxx /data xfs defaults 0 0` — what happens at boot if that disk is removed?
539. 🔴 A systemd unit has `Restart=always` and the app crashes immediately on start. What happens?
540. 🔴 `ulimit -n` shows 1024 and Nginx handles 5,000 concurrent connections. What error appears?

---

## 42. Scenario-Based Questions — Networking

541. 🟡 Your application can't connect to the database server. Walk through your troubleshooting steps (DNS, ping, port, firewall, credentials, TLS).
542. 🟡 Users report the website is down, but the server is running. How do you find the problem?
543. 🟡 An API call from your server to a partner's HTTPS endpoint fails with a TLS error. How do you troubleshoot? 💰
544. 🟡 After a DNS migration, half the users still reach the old server. Why, and what do you do?
545. 🟡 Your service intermittently times out when calling another internal service. What do you check?
546. 🟡 Outbound calls fail only from production servers, not from your laptop. What could be different (proxy, firewall, DNS, NAT)?
547. 🟡 You need to expose an internal service only to specific partner IPs. How do you design it? 💰
548. 🟡 Clients behind a load balancer all appear to come from the same IP in your logs. How do you fix it?
549. 🔴 Requests through the load balancer randomly fail with connection reset after idle time. What is happening?
550. 🔴 Your server has thousands of connections in CLOSE_WAIT. What does it mean and how do you fix it?
551. 🔴 Under load, outbound HTTP calls fail with "Cannot assign requested address". Why, and how do you fix it?
552. 🔴 Design the network for a banking application with internet banking, internal apps and databases. 💰

---

## 43. Scenario-Based Questions — Linux / RHEL Production Issues

553. 🟡 The disk on a production server is 100% full. How do you find the cause and fix it safely?
554. 🟡 The server's CPU is at 100%. How do you find the cause?
555. 🟡 The server is running out of memory and the app keeps getting killed. How do you investigate?
556. 🟡 A service fails to start after a reboot. How do you debug it?
557. 🟡 Nginx returns 502 Bad Gateway after deploying your .NET app on RHEL. Walk through all possible causes.
558. 🟡 Nginx returns 403 Forbidden for static files in a custom directory on RHEL. How do you fix it?
559. 🟡 You changed Nginx to listen on port 8443 and it fails to start. What do you check (SELinux port label, firewalld, conflicts)?
560. 🟡 A cron job that cleans logs stopped running. How do you investigate?
561. 🟡 A user can't SSH into the server. How do you troubleshoot?
562. 🟡 You need to give a developer read-only access to application logs without sudo. How do you do it (groups, ACLs)?
563. 🟡 The application gets "Too many open files" errors under load. How do you fix it?
564. 🟡 You need to add 100 GB to the `/var` filesystem on a running server using LVM. How?
565. 🟡 After a reboot, a mounted NFS share is missing and the app fails. How do you make it reliable?
566. 🟡 Time on the server is drifting and transaction timestamps are wrong. How do you fix it? 💰
567. 🔴 A kernel update caused the server not to boot. How do you recover?
568. 🔴 You forgot the root password of a RHEL 9 VM. How do you reset it?
569. 🔴 The server is very slow but CPU and memory look fine. What else do you check (I/O wait, disk latency, swap, network, D-state processes)?
570. 🔴 A security audit requires disabling root SSH login, enforcing key-based login and logging all sudo commands. How do you implement it? 💰
571. 🔴 You must deploy your .NET + Nginx stack on 20 RHEL servers consistently. How do you automate it (Ansible, Kickstart, images)?
572. 🔴 A process is using 100% CPU and you suspect an infinite loop in a .NET app. How do you diagnose it without restarting?

---

## 44. Hands-On Tasks

573. 🟢 Find your server's IP address, default gateway and DNS servers.
574. 🟢 Check which ports are listening and which processes own them.
575. 🟢 Create a user `appuser` with no login shell and a group `appgroup`.
576. 🟢 Create a directory `/opt/myapp`, give ownership to `appuser`, and set permissions to `750`.
577. 🟡 Install Nginx and the ASP.NET Core runtime on RHEL.
578. 🟡 Create a systemd service for an ASP.NET Core app and enable it at boot.
579. 🟡 Configure Nginx as a reverse proxy to `http://127.0.0.1:5000` and fix SELinux so it works.
580. 🟡 Open ports 80 and 443 permanently in firewalld.
581. 🟡 Install a TLS certificate in Nginx and redirect HTTP to HTTPS.
582. 🟡 Configure logrotate for `/var/log/myapp/*.log` to keep 14 days, compressed.
583. 🟡 Write a cron job and a systemd timer that run a cleanup script daily at 1 AM.
584. 🟡 Create an LVM volume group from two disks, create a 20 GB logical volume, format with XFS and mount it permanently via `/etc/fstab`.
585. 🟡 Extend the logical volume by 10 GB and grow the filesystem online.
586. 🟡 Configure a static IP address using `nmcli`.
587. 🟡 Set up key-based SSH and disable password login.
588. 🟡 Configure chrony to sync with an internal NTP server.
589. 🟡 Write a bash script that checks if the app's health endpoint returns 200 and restarts the service if not.
590. 🟡 Find the top 10 client IPs and top 10 URLs in an Nginx access log using shell commands.
591. 🟡 Capture traffic to port 5432 using `tcpdump` and save it to a file.
592. 🟡 Run a .NET app in a rootless Podman container using a UBI image, with a volume mount that works under SELinux.
593. 🔴 Trust an internal CA certificate system-wide and verify with `curl` and a .NET app.
594. 🔴 Add audit rules to log all changes to `/etc/nginx/` and all `sudo` usage.
595. 🔴 Scan the server with OpenSCAP against a CIS profile and fix three findings.

---

## 45. Rapid-Fire Round

596. 🟢 How many layers are in the OSI model?
597. 🟢 Which layer does IP work at?
598. 🟢 Which protocol is connection-oriented — TCP or UDP?
599. 🟢 Default port for SSH? HTTPS? PostgreSQL? SQL Server? MySQL? Oracle?
600. 🟢 What does DNS stand for?
601. 🟢 Which DNS record maps a name to an IPv4 address?
602. 🟢 How many usable hosts are in a /24?
603. 🟢 What is the loopback address?
604. 🟢 Which command shows IP addresses on RHEL?
605. 🟢 Which command shows listening ports?
606. 🟢 Which command manages services on RHEL?
607. 🟢 Which command installs packages on RHEL 9?
608. 🟢 What is the default filesystem in RHEL?
609. 🟢 What is the default firewall service in RHEL?
610. 🟢 What is the command to check SELinux mode?
611. 🟢 What does `chmod 755` mean?
612. 🟢 Which file stores user password hashes?
613. 🟢 Which signal does `kill` send by default?
614. 🟢 Which command shows disk usage of filesystems?
615. 🟢 Which command shows the size of a directory?
616. 🟡 Which command shows logs of a systemd service?
617. 🟡 Which command makes a firewalld change persistent?
618. 🟡 Which SELinux boolean allows Nginx to connect to a backend?
619. 🟡 Which command restores default SELinux file contexts?
620. 🟡 Which command adds an SELinux port label?
621. 🟡 Which command reloads systemd unit files?
622. 🟡 Which command extends an LV and its filesystem in one step?
623. 🟡 Which tool configures networking from the command line in RHEL?
624. 🟡 Which command adds a CA certificate to the system trust store?
625. 🟡 Which container tool is the default on RHEL?
626. 🟡 Which TCP state indicates the application hasn't closed the socket?
627. 🟡 Which TCP state remains after the side that closes first finishes?
628. 🔴 What is the difference between `systemctl stop` and `systemctl mask` in one line?
629. 🔴 What is the difference between `chcon` and `semanage fcontext` in one line?
630. 🔴 What is the difference between a security group and a network ACL in one line?
631. 🔴 What is the difference between SNAT and DNAT in one line?

---

> **Series:** Part 1 — C# · Part 2 — .NET Core, Web API & MVC · Part 3 — EF Core · Part 4 — ADO.NET · Part 5 — Authentication & Authorization · Part 6 — Microservices, Nginx & IIS · Part 7 — Kafka & Event-Driven Architecture · Part 8 — Relational Databases · Part 9 — Backend Engineering Fundamentals · Part 10 — System Design · Part 11 — Networking & Red Hat Linux.
