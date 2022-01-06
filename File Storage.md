(Music) In this video, we’re going to talk about File Storage in greater detail.
Like direct attached storage, file storage must be attached to a compute node
before it can be accessed and have data stored on it. However, File Storage can
be less expensive, more resilient to failure, and involve lesser disk management
and maintenance for you as the user to do , as compared to direct attached
storage. You can also provision much larger amounts of File Storage and present
it as a disk to a server. File storage is mounted from remote storage
appliances. That is, the physical disks are contained in a separate, specialised
piece of hardware and they are then connected to the compute node via the
underlying infrastructure in the datacenter. These storage appliances are not
only extremely resilient to failure, the data is also far more secure in them as
these storage appliances offer services such as encryption in transit and
encryption at rest. These appliances are all managed by the service provider.
File Storage is mounted to compute nodes via an ethernet network – the same kind
of network that you might receive email or browse the internet over, although
this ethernet network is normally dedicated to the task. This means it can
sometimes be referred to as ‘Network Attached Storage’, ‘Network File Storage’
or simply ‘NFS. One of the issues with ethernet networks is that their speed can
vary – the more loaded an ethernet network is, the more likely it becomes that
it’s speed or bandwidth will be affected. Of course, Cloud Providers build their
storage networks to handle very high volumes of traffic. But even so, consistent
speed cannot be guaranteed. Therefore, File storage tends to be used for
workloads where consistently high network speeds are not a requirement. In terms
of workloads, File Storage can typically be mounted onto more than one compute
node at a time, where the mounted disk or volume looks just like another drive
on the compute node. The ability for File Storage to be mounted to multiple
compute nodes at a time make it an ideal solution where some sort of common
storage is required – for example, a departmental file share, a ‘landing zone’
for incoming files that need to be processed by an application, or a repository
of files that a web service might access. In these applications, the potential
variance in the speed of the connecting network is not really an issue. Of
course, where cost is an issue, you can use file storage for other applications
such as databases, but the trade-off is speed. When you provision file storage,
one consideration you need to take into account is the IOPS capacity of the
storage. IOPS stands for Input/Output Operations Per Second and refers to the
speed at which the disks can write and read data (note this is not the speed of
the network between the storage and the compute node). The higher the IOPS
value, the faster the speed of the underlying disk. A higher IOPS will also
normally cost more. Understanding IOPS is important because if the IOPS value is
too low for your application, the storage can become a bottleneck and cause your
application to run slowly. Alternatively, if the IOPS is too high, you will
probably be paying more that you need to for your storage. For example, a file
share may be mounted on 30 different compute nodes and an application writes and
requests data to and from that share 60 times per minute. You can average that
out to 1 operation per second. With this simple example, you can see that each
application has different IOPS requirements. In the next video, we’re going to
talk more about Block Storage, how it compares with File Storage, and when you
would typically use one over the other.