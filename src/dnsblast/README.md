# DNS Blast

An adoption of DNS Stress tool to validate the DNS server throughput.
Original source codes: [https://github.com/sandeeprenjith/dnsblast](https://github.com/sandeeprenjith/dnsblast).

Heavily relies on the idea of [Distinct Heavy Hitter attack](https://faculty.idc.ac.il/bremler/Papers/HotWeb_18.pdf):

Sends DNS queries with QType set to 'A'.

## Job parameters

* `root_domain` - Root domain to use which will be queried for nameservers
* `protocol` - DNS net. protocol (`udp` as default, [`udp`, `tcp`, `tcp-tls`] supported)
* `seed_domains` - Domain names to use as base of DNS query (no default, at least one required, like `yahoo.com`)
* `parallel_queries` - Number of DNS queries to send between delays
* `interval_ms` - (inherited) delay in MS between query loop iteration 
