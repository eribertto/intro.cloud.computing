(Music) In this video, we’re going to start to understand what Object Storage
is, how data is stored in Object Storage, and how it differs from the more
traditional storage types such as File and Block Storage. The first thing to
note about Object Storage is that you do not connect it to a particular compute
node in order to use it. Instead, you provision an Object Storage service
instance and use an API (or Application Program Interface) to upload, download,
and manage your data. This means you can directly use Object Storage with
anything that can call an API and you don’t need an underlying compute node. The
second thing to note about Object Storage is that it’s less expensive that other
cloud storage options. It’s per gigabyte cost is typically a couple of US cents
per month and in some cases, even less, depending on the storage tier used. More
on storage tiers later. The third and possibly most important thing to note
about Object Storage is that it’s effectively infinite. With file and block
storage, you specify the size of the storage you want in gigabytes or terabytes
and then pay a fee based on the size you provisioned. With Object Storage, you
just consume the storage you need and pay per gigabyte cost for what you use.
You can keep uploading files and the storage will never run out. So, when would
you use Object Storage? Well, Object Storage is great for storing large amounts
of unstructured data. By unstructured this means that the data is not stored in
any kind of hierarchical folder or directory structure – Object Storage uses
‘buckets’, and objects are stored within these buckets in a structurally flat
way. A bucket is a bit like a folder, in the sense that you can give them
meaningful names, and of course have different buckets for different
object-types but you cannot place a bucket within a bucket. When an object is
placed in a bucket, it also has some metadata (data about the data) added to it,
such as an object ID. This metadata helps applications to both locate and access
the object, as well as provide information on the time that the data was stored
or last accessed. When you create a bucket, you don’t need to provide or define
any sizing information. The bucket will just hold the data that you place inside
it and the service provider ensures that there is sufficient storage capacity
available. Buckets can hold as little as a few bytes of data, right up to
multiple petabytes and you can build up the amount of data stored as slowly or
quickly as you like, as well as shrink it back down again. The service provider
also takes care of resilience and making sure that the Object Storage solution
is highly available. Some cloud providers offer different types of buckets with
different levels of resilience. For example, they offer buckets which are
resilient, but the data is only stored in one data centre. This is a good option
where data needs to reside in a particular geographical location or in
situations where high availability is less of an issue. They will then offer
buckets which are highly available across regions, where the data is stored
multiple times in different datacentres (or zones) in the same region or even in
multiple regions. These options usually cost more but they provide both the
highest level of resilience as well as availability for your data. Object
Storage has a very ‘flat’ storage structure, which we’ll explain in the next
lesson. This data can be anything from text files to audio and video files, from
IOT data to virtual machine images, from backup files to data archives. Pretty
much any data which is static and where fast read and write speeds are not
necessary would make a good fit for object storage. Object Storage would,
however, not be suitable for running operating systems, nor applications such as
databases or anything else where the contents of the files changes. So, to
summarize what we have learned in this lesson: Object Storage is used to store
files or Objects which are static. The data that you can store using Object
Storage can be anything from text files to audio and video files, from IOT data
to virtual machine images, from backup files to data archives. You cannot run
operating systems or other applications such as databases using Object Storage.
Objects are stored in Buckets. You can have multiple buckets, but you cannot
place buckets within buckets. You do not need to specify a size for a bucket,
you can just use as little or as much space as you need. Many providers offer
different types of buckets with different charges for each. Some are based on
resilience and availability, while others are based on the frequency at which
the objects inside are accessed. In the next video, we’ll be diving into Object
Storage data tiers and Object Storage APIs.