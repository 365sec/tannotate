tannotate
=========
 
你必须先拥有 AS、BGP相关的知识 

tannotate is a golang-based utility that facilitates annotating large datasets
with additional network metadata. Right now this includes:

 * Maxmind GeoIP2
 * AS/Routing Data (based on an MRT routing table)

For example, you can add Maxmind geolocation data to a list of IPs:

	cat ips.csv | tannotate --geoip2 --geoip2-database=geoip2.mmdb
        
	
	cat ips.csv | tannotate --input-file=/home/docker/gobgp_1.29_linux_amd64/ips.txt  --routing --mrt-file=/home/docker/gobgp_1.29_linux_amd64/latest-bview    --as-names=/home/docker/gobgp_1.29_linux_amd64/as.json 
	
	
	
 note latest-bview   download from  http://data.ris.ripe.net/rrc01/
