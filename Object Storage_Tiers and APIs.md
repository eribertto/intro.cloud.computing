[MUSIC] In this video, we're going to look more closely at Object Storage data
tiers and Object Storage APIs. Object Storage buckets also have storage tiers,
or classes, associated with them, and these tiers are based on how frequently
the data is accessed. A standard tier bucket is where you would store objects
that are frequently accessed. This tier tends to have the highest per gigabyte
cost associated with it. A vault or archive tier is where you might store
documents that are only accessed perhaps only once or twice a month, or less,
and this will be offered at a lower storage cost. Whereas there may also be cold
vault tier, where you would store data that is typically accessed only once or
twice a year. This storage often costs just a fraction of a US cent per gigabyte
per month. Often, you can also set up automatic archiving rules for your data,
meaning that if an object isn't accessed for a period of time, it will
automatically be moved to a cheaper storage tier. The rule uses some of the
object's metadata to determine when it should be archived. Note that, Object
Storage does not come with IOPS options. Object Storage tends to be very slow in
comparison with file or block storage, where downloads typically takes seconds
if not longer to complete. Where providers offer cold vault buckets, data
retrieval from these tiers can sometimes even take hours because the storage is
kept offline. If your application needs fast access to files, then object
storage may not be a good option. We've mentioned that object storage is priced
per gigabyte used, but there can also be other costs related to retrieval of the
data. These costs are similarly low, but access charges can be higher for data
that is in a vault or cold vault tiers, so it is important to ensure that the
data is in the correct tier based on its frequency of access. Object Storage
does not need to be attached to a compute node for you to access it, rather you
access object storage through an application program interface, or API. The most
common API for object storage is called the S3 API, which is a standard based on
the S3 object storage offered by AWS. Many providers offer APIs to their object
storage, which is S3 compatible, which is useful, because it means developers
can write code which is able to access multiple vendors object storage. The API
itself is an HTTP based RESTful API, or RESTful web service. The API call allows
applications to manage object storage and buckets, as well as put, upload, or
get download objects to and from them. Object Storage is not just for new
applications, but can be used to meet requirements for existing ones. It can
also be used as an effective solution for backup and disaster recovery as a
replacement for off-site tape based solutions, reducing the time to restore
data. Many backup packages now include the ability to backup data up into the
Cloud using object storage. Object Storage is more efficient than tape backup
solutions, which require tapes that need to be physically loaded into, and
removed from, tape drives and moved off-site for geographical redundancy. So, to
summarize what we have learned in this lesson, object storage has different
tiers with different charges for each. Some are based on the frequency at which
the objects inside are accessed. Object Storage is priced per gigabyte of
storage used per month plus some charges for data retrieval. Object Storage is
much cheaper than file or block storage. Object Storage is very slow in
comparison with file and block storage. You can often create rules which allow
the automatic archiving of objects to cheaper tiers when they are in frequently
accessed. Object Storage is accessed using an API. Many Object Storage providers
have an S3 compatible API which means developers can create code that will work
against multiple vendor Object Storage solutions. Object Storage in the Cloud
offers an effective Backup and Disaster Recovery Solution. In the next video, we
will be covering Content Delivery Network, or CDN, which is driven by Object
Storage. [MUSIC]