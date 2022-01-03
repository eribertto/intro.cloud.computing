(Music) Virtual Machines or VMs are also known as Virtual Servers or Virtual
Instances, or simply Instances, depending on the cloud provider. The various
cloud providers make VMs available in a variety of configurations and deployment
options to serve different use cases. When you create a virtual server in the
cloud, you specify the Region and Zone or Data Center you want the server to be
provisioned in and the Operating System you want on it. You can choose between
shared (that is, a multi-tenant) VMs or dedicated (that is, a single-tenant)
VMs. You can also choose between hourly or monthly billing, and select storage
and networking options for the virtual server. Now let’s look at a few different
types of VMs that can be provisioned in the cloud. Shared or Public Cloud VMs
are provider-managed, multi-tenant deployments that can be provisioned on-demand
with predefined sizes. Being multi-tenant means that the underlying physical
server is virtualized and is shared across other tenants or users. To satisfy
different workloads, cloud providers offer predefined sizes and configurations
ranging from a single virtual core and a small amount of RAM to multiple virtual
cores and much larger amounts of RAM. For example there can be configurations
for Compute Intensive workloads, Memory intensive workloads, or High Performance
I/O. Rather than pick from only pre-defined sizes, some providers also offer
custom configurations that allow users to define the number of cores and RAM and
local storage characteristics. Public VMs are usually priced by the hour (or in
some cases even seconds) and configurations start as low as pennies per hour.
Some providers also let you get monthly VMs, which can result in some cost
savings if you know you will run the VM for at least a month, but if you decide
to de-commision the VM in the middle of the month, you will still be charged for
the full month. Transient or Spot VMs take advantage of unused capacity in a
cloud data center. Cloud providers make this unused capacity available to users
at a much lower cost than regular VMs of similar sizes. Although the Transient
VMs are available at a huge discount, the Cloud provider can choose to
de-provision them at any time and reclaim the resources for provisioning
regular, higher-priced, VMs. Because you run the risk of losing these VMs when
capacity in the data center decreases, these VMs are great for non-production
workloads such as testing and developing applications. They are also useful for
running stateless workloads, testing scalability, or running big data and high
performance computing (HPC) workloads at a low cost. Reserved virtual server
instances allow you to reserve capacity and guarantee resources for future
deployments. You reserve desired amount of virtual server capacity, provision
instances from that capacity when you need them, and choose a term, such as 1
year or 3 years, for your reserved capacity. You're guaranteed this capacity
within the data center of your choice for the life of the contract term. By
committing to a longer term, you can also lower your costs compared to hourly or
monthly instances. This can be useful when you know you require at least a
certain level of cloud capacity for a specific duration. If you exceed your
reserved capacity, you can always choose to supplement your unplanned usage and
capacity requirements with hourly or monthly VMs. Note however that not all
predefined VMs families or configurations may be available as reserved.
Dedicated hosts offer single-tenant isolation. This means that only your VMs run
on a given host so they can make exclusive use of full capacity and resources of
the underlying hardware. When provisioning a dedicated host you to specify the
data center and POD in which you want your host placed. You then assign
instances, or virtual machines, to a specific host. This allows for maximum
control over workload placement. Dedicated hosts are typically used for meeting
compliance and regulatory requirements or meet specific licensing terms.
Virtualization and VMs are at the center of cloud computing and provide many
benefits. In the next video, we will discuss bare metal servers, what they are
and what they provide.