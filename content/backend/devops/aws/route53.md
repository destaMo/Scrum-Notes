# Route53

Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service.

- Reliable and cost-effective way to route end users to Internet applications
- Supports **multi-region and backup architectures for High availability. ELB, limited to region, does not support multi region HA architecture**
- supports private Intranet facing DNS service
- **internal resource record sets only work for requests originating from within the VPC** and currently cannot extend to on-premise
- Global propagation of any changes made to the DNS records within ~ 1min
- Route 53 to create an alias resource record set that points to ELB, S3, CloudFront. An alias resource record set is an Route 53 extension to DNS. It's similar to a CNAME resource record set, but supports both for root domain - zone apex e.g. example.com, and for subdomains for e.g. www.example.com.
- CNAME resource record sets can be created only for subdomains and cannot be mapped to the zone apex record
- **Routing policy**
  - Simple routing ? simple round robin policy
  - Weighted round robin ? assign weights to resource records sets to specify the proportion for e.g. 80%:20%
  - Latency based routing ? helps improve global applications as request are sent to server from the location with minimal latency, is based on the latency and cannot guarantee users from the same geographic will be served from the same location for any compliance reasons
  - Geolocation routing ? Specify geographic locations by continent, country, state limited to US, is based on IP accuracy
  - Failover routing ? failover to a backup site if the primary site fails and becomes unreachable
- **Weighted, Latency and Geolocation can be used for Active-Active while Failover routing** can be used for Active-Passive multi region architecture

> [Service overview](https://aws.amazon.com/route53/)
