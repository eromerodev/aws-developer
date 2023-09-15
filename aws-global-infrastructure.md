# AWS Global Infrastructure

This table provides a concise overview of the different elements that make up AWS Global Infrastructure, each with its own set of advantages and typical use cases.

| Component | Description | Example Use Cases |
| --- | --- | --- |
| Regions | Geographically isolated areas with multiple, redundant availability zones. | Data residency, low-latency access |
| Availability Zones (AZs) | Data centers within a region that are designed to be isolated from failures in other AZs. | High availability, fault tolerance |
| Edge Locations | Physical locations deployed closer to end users to enable low-latency and high-speed data transfer. | Content delivery, DNS resolution |
| Local Zones | Infrastructure deployments that extend AWS services closer to end-users in specific cities or locations. | Ultra-low latency applications |
| Wavelength Zones | Extensions of Availability Zones located within telecommunication carriers' data centers. | Mobile edge computing |
| Outposts | Fully managed service that extends AWS infrastructure to on-premises for a truly hybrid experience. | Local data processing, low-latency |

> Each AWS Region is a separate geographic area. Each AWS Region has multiple, isolated locations known as Availability Zones.
