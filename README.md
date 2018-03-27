tannotate
=========
 
你必须先拥有 ANS、BGP相关的知识 
```
BGP是自治系统间的路由协议，BGP交换的网络可达性信息提供了足够的信息来检测路由回路并根据性能优先和策略约束对路由进行决策。
```
全球as2.0
```
http://www.cidr-report.org/as2.0/autnums.html
```
 
全球MRT TABLE_DUMPv2 file 数据
```
 http://data.ris.ripe.net/rrc01/
```


tannotate is a golang-based utility that facilitates annotating large datasets
with additional network metadata. Right now this includes:

 * Maxmind GeoIP2
 * AS/Routing Data (based on an MRT routing table)

For example, you can add Maxmind geolocation data to a list of IPs:

	cat ips.csv | tannotate --geoip2 --geoip2-database=geoip2.mmdb
        
	
	cat ips.csv | tannotate --input-file=/home/docker/gobgp_1.29_linux_amd64/ips.txt  --routing --mrt-file=/home/docker/gobgp_1.29_linux_amd64/latest-bview    --as-names=/home/docker/gobgp_1.29_linux_amd64/as.json 
	
	
