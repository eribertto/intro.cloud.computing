(Music) After choosing the cloud service model and the cloud type offered by
vendors, customers need to plan the infrastructure architecture. The
infrastructure layer is the foundation of the cloud. This layer consists of
physical resources that are housed in Regions, Zones and Data Centers. A Cloud
provider’s IT environment is typically distributed across many regions around
the world. A cloud region, is a geographic area or location where a cloud
provider’s infrastructure is clustered, and may have names like NA South or US
East. The cloud regions are isolated from each other so that if one region was
impacted by a natural disaster like an earthquake, the cloud operations in other
regions would keep running. Each Cloud Region can have multiple Zones (or
Availability Zones or AZ for short), which are typically distinct Data Centers
with their own power, cooling and networking resources. These Zones can have
names like DAL-09 or us-east-1. The isolation of zones improves the cloud’s
overall fault tolerance, decreases latency, and avoids creating a single shared
point of failure. The Availability Zones (and DataCenters within them) are
connected to other AZs and regions, private datacenters and the Internet using
very high bandwidth network connectivity. A cloud data center is a huge room or
a warehouse containing cloud infrastructure. These data centers contain pods and
racks or standardized containers of computing resources such as servers, as well
as storage, and networking equipment - virtually everything that a physical IT
environment has. Computing Resources: Cloud providers offer several compute
options – Virtual Servers, Bare Metal Servers, and “Serverless” computing
resources. Most of the servers in a cloud datacenter run hypervisors to create
virtual servers or virtual machines (also called VMs for short), that are
software-based computers, based on virtualization technologies. Other servers in
the racks are bare metal servers that are physical servers that aren’t
virtualized. Customers can provision VMs and Bare Metals servers as and when
they need them and run their workloads on them. Cloud users can also run their
workloads on serverless computing resources, which are an abstraction layer on
top of virtual machines. We will talk about all three compute options in greater
detail in subsequent videos. Storage: Information and data can consist of files,
code, documents, images, videos, backups, snapshots, and databases and can be
stored in many different types of storage options on the Cloud. Bare Metal
Servers and Virtual Servers are provisioned with default storage in local
drives. Since these cloud servers can be provisioned and decommissioned by
customers on demand and freed up for use by other users, any information stored
in a local drive can be lost when you delete or decommission a cloud server.
However there are other storage options available on the cloud to persist data
that you can choose depending on factors like how important your data is, how
quickly you want to be able to access it, how often you access it, and how
secure you need it to be. These additional storage options include Block
storage, File storage, and Object storage. Block and file storage modes are
commonly used in traditional data centers, but often struggle with scale,
performance and distributed characteristics of cloud. Object storage is the most
common mode of storage in the cloud as it’s both highly distributed and
resilient. We will examine Object Storage and the other storage options in more
detail in later videos. Networking: Networking infrastructure in a cloud data
center includes traditional networking hardware like routers and switches, but
more importantly for users of the Cloud, the Cloud providers have Software
Defined Networking (or SDN) options where certain networking resources are
virtualized or made available programmatically, through APIs. This allows for
easier network provisioning, configuration, and management in the cloud. When
servers in the cloud are provisioned, you need to setup their public and private
network interfaces. The public network interfaces, as the name suggests, connect
the servers to the public internet, whereas the private ones provide
connectivity to your other cloud resources and help keep them secure. As in the
physical IT world, network interfaces in the cloud need to have IP addresses and
subnets either assigned automatically or configured. In a cloud environment it
is even more important to configure which network traffic and users can access
your resources, which can be done by setting up Security Groups and Access
Control Lists (or ACLs). For further security and isolation of your resources in
the cloud, most Cloud providers provide Virtual Local Area Networks (VLANs),
Virtual Private Clouds (VPCs), and Virtual Private Networks (VPNs). Some of the
traditional hardware appliances such as firewalls, load balancers, gateways and
traffic analyzers can also be virtualized and made available as services in the
cloud. Another networking capability provided by the Cloud Providers is Content
Delivery Networks or CDNs, that distribute content to multiple points throughout
the world so users accessing the content can access it more quickly by getting
it from a point nearest to them. We will learn more about some of these cloud
networking options and terminology in subsequent videos. Cloud infrastructure is
constantly advancing and improving. In the next video, we explain virtualization
and virtual machines.