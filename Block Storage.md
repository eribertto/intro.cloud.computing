(Music) In this video, we will discuss Block Storage and how it compares to File
Storage in the Cloud. Block storage breaks files into chunks (or blocks) of data
and Stores each block separately under a unique address. Like direct attached
storage and file storage, block storage also must be attached to a compute node
before it can be utilized for your workloads. Block storage, like file storage,
can be mounted from remote storage appliances, making it extremely resilient to
failure, and keeping data far more secure in them, on account of encryption in
transit, and encryption at rest services, available on these appliances. Block
storage is mounted as a volume to compute nodes using a dedicated network of
fibres, through which signals move at the speed of light. These fibre optic
networks are more expensive to build than the ethernet ones which deliver File
Storage, which is one reason why Block Storage tends to have a higher
price-point. However, since the traffic is moving faster and with speed
consistency, they are perfect for workloads that need low-latency storage to
work effectively. In terms of workloads, it is important to note that unlike
File Storage, which can be mounted onto 80 computer nodes or more, Block storage
is normally mounted onto only one compute node at a time. Since these disks run
at a consistent high speed, they are perfect for workloads that need
consistently fast storage, such as databases and mail servers. Block storage is
not suitable for workloads where there needs to be some level of disk sharing
between compute nodes. For block storage, as it is for file storage, you need to
take the IOPS capacity of the storage into account. Most cloud providers will
allow you to specify IOPS characteristics when you provision storage and, in
some cases, adjust the IOPS of your storage as you need, so if the requirements
or usage behaviour of an application changes, you can adjust accordingly. So, to
summarise the commonalities and differences between these two storage types:
Block and File Storage is taken from appliances which are maintained by the
service provider. Both are normally highly available and resilient and will
often include data encryption at rest and in transit. File storage is attached
to compute nodes using an ethernet network, so it is sometimes called Network
attached or NFS Storage. File storage is very reliable, but the speed of the
connecting network can vary, based on load. Block storage is attached via a
high-speed fibre network, which is very reliable and consistent. File storage
can be attached to multiple compute nodes at once. Block storage can only be
attached to one node at a time. File storage is a good choice where file shares
are required, where workloads do not require lightning fast connectivity to
storage, or where cost is a factor. Block storage is a good choice when
supporting an application that needs consistent fast access to disk, such as
databases. Remember to consider the IOPS requirements of the application when
provisioning either file or block storage. In the next video, we’ll start to
look at Object Storage.