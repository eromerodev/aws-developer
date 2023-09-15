# AWS Global Infrastructure

Infrastructure, like data centers and networking connectivity, still exists as the foundation of every cloud application. In AWS, this physical infrastructure makes up the AWS Global Infrastructure, in the form of Regions and Availability Zones.

| Name                   | Description                                                                                                   |
| ---------------------- | ------------------------------------------------------------------------------------------------------------- |
| Region                 | An AWS Region is a physical location where AWS will host a cluster of data centers                                      |
| Availability Zone (AZ) | One or more data centers that are physically separate and isolated from other AZs                             |
| Edge Location          | A location with a cache of content that can be delivered at low latency to users (used by CloudFront)         |
| Regional Edge Cache    | Also part of the CloudFront network. These are larger caches that sit between AWS services and Edge Locations |
| Global Network         | Highly available, low-latency private global network interconnecting every data center, AZ, and AWS region    |


>  Each AWS Region is a separate geographic area. Each AWS Region has multiple, isolated locations known as Availability Zones.

### Availability Zone

Inside every Region is a cluster of Availability Zones (AZs). An AZ consists of one or more data centers with redundant power, networking, and connectivity. These data centers operate in discrete facilities in undisclosed locations. They are connected using redundant high-speed and low-latency links.
