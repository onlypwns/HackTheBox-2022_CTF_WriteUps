# Forensics - trick or breach

`tshark -Y "dns.flags.response == 0" -T fields -e "[dns.qry.name](http://dns.qry.name/)" -e "[dns.qry.name](http://dns.qry.name/)" -r capture.pcap | cut -d '.' -f1 | tr -d '\n' | xxd -r -p > dns_subdomains`

All we had to do is run this command and get the HEX output brah

Flag: `HTB{M4g1c_c4nn0t_pr3v3nt_d4t4_br34ch}`
