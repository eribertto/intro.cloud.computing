(Music) Cloud storage is where you save data and files in the cloud. Certain
storage must be attached to a compute node before the storage can be accessed,
whereas other storage types can be directly accessed either through the public
Internet or a dedicated private network connection. Cloud providers host,
secure, manage, and maintain the cloud storage and associated infrastructure to
ensure you have access to your data when you need it. Cloud storage services
allow you to scale your capacity as you need so you only pay for what you
provision, usually on a ‘per gigabyte’ basis. The cost of storage will vary by
type but in general, the faster the read / write speed of the storage, the
higher the per gigabyte cost. Cloud storage is available in four main types –
Direct Attached, File Storage, Block Storage and Object Storage. Direct Attached
storage, sometimes referred to as ‘Local Storage’, is storage which is presented
directly to a cloud-based server and is effectively either within the host
server chassis or within the same rack. This storage is fast and normally only
used to store a server’s operating system, although it can have other use
cases.The main two reasons why direct attached storage is not so great for other
uses besides to store the operating system is that it’s typically ‘Ephemeral’ ,
meaning that it only lasts as long at the compute resource it’s attached to – it
cannot be shared with other nodes and while you can use RAID techniques, it’s
not as resilient to failure as other types of storage. File storage is typically
presented to compute nodes as ‘NFS Storage’. NFS stands for Network File System
and means that the storage is connected to compute nodes over a standard
ethernet network. NFS-mounted storage is common-place but it tends to be slower
than either direct-attached storage or block storage because the data travels
over an ethernet network. It also tends to be lower cost than either direct
attached or block storage. One advantage of File Storage is that it can be
mounted or used on multiple servers at once. File-based storage is a simple,
straightforward approach to data storage and works well for organizing data in a
hierarchical folder structure, that desktop users are familiar with. Block
storage is presented to compute nodes using high-speed fibre connections, which
means that read and write speeds are typically much faster and reliable than
with file storage, making block storage suitable for use with databases and
other applications where disk speed is important. You typically provision block
storage in ‘volumes’, which can then be mounted onto a compute node, which it
then effectively sees as another hard drive. Volumes can normally only be
mounted onto one compute node at a time. With both File and Block storage, you
may also hear the term ‘IOPS’. IOPS stands for ‘Input/Output Operations Per
Second’ and relates to the speed of the storage or to put it another way, how
quickly data can be read from or written to the storage. We’ll cover this in a
little more detail in a later video. Persistence is a term that is used when
provisioning File or Block storage and relates to what happens to the storage
once the compute node it is attached to is terminated. If the storage is set to
‘persist’ then it will not be deleted along with the compute node, meaning that
it and its data are preserved and available to mount onto another compute node,
though you will continue to pay for the storage. You can also, in some cases,
set the storage so that it is automatically deleted with the compute node that
it is mounted onto – in this case, as we know, it becomes Ephemeral Storage.
Here, you will also stop paying for the storage but you will lose any data
unless it is backed up somewhere. There are several ways to backup data in the
cloud but one way to back up both File and Block storage is to take a Snapshot.
As the term implies, this is a point in time image of the storage. Snapshots are
usually fast to create (they don’t actually write any data, or rather they
create metadata), don’t require downtime and subsequent snapshots record only
changes to the data. They are great for returning storage to the way it was at a
particular snapshot, though note, they cannot be used to recover individual
files. The fourth kind of storage is Object storage. This is a different type of
storage in so much as it’s not attached to a compute node, rather it is accessed
via an API. Of all the storage types, Object Storage is by far the cheapest and
also the slowest in terms of read and write speeds, but it is infinite in size
to the end user. Unlike File and Block storage where you provision a certain
storage capacity and it fills up over time, with Object Storage you can keep
adding files to it and it never fills up, you just pay for what you use. This
makes Object Storage a fantastic repository for all sorts of unstructured data
types, large and small, including documents, video, logs, backups, data from
IoT, application binaries and virtual machine images. In the following videos,
there will be more detailed information on the different types of storage.