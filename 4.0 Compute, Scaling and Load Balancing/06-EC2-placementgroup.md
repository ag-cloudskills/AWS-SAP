# EC2 placement groups

- Cluster -> pack instances, high performance , instances are launched at one time( recommended), lock the instances in AZ, fast bandwidth , 10 GBbs stream rate,lowest latency, max pps, right instance type ( enhanced network) , trade off resilience, can span vpc peers in same region

- Spread -> Keep instances separated, multi AZ, distinct racks, 7 instances per AZ ( hard limit), infrastructure isolation,dedicated host not supported, for critical applications

- Partition -> groups of instances spread apart, more than 7 instances per AZ, max 7 partition per AZ , required for parallel processing. intelligent data replication as per partition, topology aware applications such as HDFX , HBase and cassandra