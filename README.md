# panwdbl-actions

*WARNING: USE THIS REPO AT YOUR OWN RISK*

panwdbl implemented with Github Actions based on ideas from [https://github.com/alex/nyt-2020-election-scraper](https://github.com/alex/nyt-2020-election-scraper)

## Details

- each IOC feed has a correspending Github Action workflow and a dedicated branch
- the workflows are triggered based on the schedule specified in each workflow YAML file
- each workflow:
    * checkouts the branch of the feed
    * grabs the original IOC feed
    * process the IOC feed using a dedicated script contained in the branch
    * if there are changes, a commit & push is performed to update the repo contents

## Feeds

| Feed | Description | URL |
| ---- | ----------- | --- |
| DShield Top 20 | DShield.org Recommended Block List | https://raw.githubusercontent.com/jtschichold/panwdbl-actions/dshield/dshieldbl.txt |
| Tor Exit Nodes | List of Tor Exit Nodes from https://www.dan.me.uk/tornodes | https://raw.githubusercontent.com/jtschichold/panwdbl-actions/dshield/dshieldbl.txt |
| SSL Abuse IP List | SSLBL 30 days block list. See https://sslbl.abuse.ch/blacklist/ | https://raw.githubusercontent.com/jtschichold/panwdbl-actions/sslabuseiplist/sslabuseiplist.txt |
| Emerging Threats Known Compromised Hosts | See https://doc.emergingthreats.net/bin/view/Main/CompromisedHost | https://raw.githubusercontent.com/jtschichold/panwdbl-actions/etcompromised/etcompromised.txt |


## Missing panwdbl Feeds

Some of the feeds that use to be available on pandwbl haven't be ported to this incarnation. Details below:

| Feed | Description | URL | Notes |
| ---- | ----------- | --- | ----- |
| Spamhaus DROP | DROP (Don't Route Or Peer) and EDROP are advisory "drop all traffic" lists, consisting of stolen 'hijacked' netblocks and netblocks controlled entirely by criminals and professional spammers. See http://www.spamhaus.org/drop/. | https://www.spamhaus.org/drop/drop.txt | Use the original URL |
| Spamhaus DROP | DROP (Don't Route Or Peer) and EDROP are advisory "drop all traffic" lists, consisting of stolen 'hijacked' netblocks and netblocks controlled entirely by criminals and professional spammers. See http://www.spamhaus.org/drop/. | https://www.spamhaus.org/drop/edrop.txt | Use the original URL |
| BruteForceBlocker | See http://danger.rulez.sk/index.php/bruteforceblocker/ | http://danger.rulez.sk/projects/bruteforceblocker/blist.php | Use the original URL |
| Malware Domain List | See http://www.malwaredomainlist.com/ | http://www.malwaredomainlist.com/hostslist/ip.txt | Seems inactive |
| Emerging Threats RBN | Emerging Threats RBN rules. | Inactive | Inactive |
| Zeus Tracker Bad IPs List | abuse.ch ZeuS IP blocklist "BadIPs" (excluding hijacked sites and free hosting providers). See https://zeustracker.abuse.ch/blocklist.php | Inactive | Inactive |
