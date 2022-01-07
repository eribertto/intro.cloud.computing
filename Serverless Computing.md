(Music) Serverless is an approach to computing that offloads responsibility for
common infrastructure management tasks such as scaling, scheduling, patching,
and provisioning application stacks to cloud providers, allowing developers to
focus their time and effort on the code and business logic specific to their
applications or process. Serverless doesn’t mean there are no servers; only that
the management of the underlying physical or virtual servers is removed from
their users. The serverless computing environment allocates resources as needed
for the applications. Let’s look at some key attributes that distinguish
serverless computing from other compute models. The serverless model requires no
provisioning of servers, installation of application stacks and software, or
operation of the infrastructure by the developer. Serverless computing runs code
only on-demand on a per-request basis, scaling transparently with the number of
requests being served. Serverless enables end users to pay only for resources
being used, never paying for idle capacity, which is unlike virtual servers on
the cloud—where end users pay for VMs as long as they are running even if idle.
Effectively, serverless abstracts the infrastructure away from developers. Code
is executed as individual functions where each function runs inside a stateless
container. No prior execution context is required to serve a request; and with
each new request, a new instance of the function is invoked. Let’s look at a
scenario. You could, for example, have a serverless platform between the
front-end of your website and your storage layer, running individual functions.
The serverless app could be translating text files and storing it in a
cloud-based storage service. Using the front-end of your website, you send text
files to a serverless app. The app creates translations in different languages,
and then stores these translated files in cloud storage, and sends their links
back to you. Some of the key serverless computing services today include IBM
Cloud Functions (which is based on Apache OpenWhisk), AWS Lamb-da, and Microsoft
Azure Functions. It is important to note that serverless may not be the best fit
for all applications or scenarios. You need to evaluate application
characteristics and ensure that the application is aligned to serverless
architecture patterns. Applications that qualify for a serverless architecture
include some of the following characteristics: Short-running stateless functions
(seconds or minutes). Seasonal workloads with varying off-peak and peaks.
Production volumetric data that shows too much idle time. Event-based processing
or asynchronous request processing for implementing use cases. Microservices
that can be built as functions that are stateless. Serverless architectures are
well-suited for use cases around data and event processing, IoT, microservices,
and mobile backends. Given its inherent and automatic scaling, rapid
provisioning, and a pricing model that does not charge for idle time, supporting
microservices architecture has become one of the most common use cases of
serverless computing today. Serverless is well-suited to working with structured
text, audio, image, and video data around tasks such as data enrichment,
transformation, validation and cleansing, PDF processing, audio normalization,
thumbnail generation, and video transcoding. Parallel tasks such as data search
and processing, and genome processing, are also well-suited to be run on a
serverless runtime. Serverless is also well-suited for working with all sorts of
data stream ingestions, including business data streams, IoT sensor data, log
data, and financial market data. And finally, let’s look at some challenges
worth considering about serverless. Serverless workloads are designed to scale
up and down in response to workload, but for workloads characterized by
long-running processes managing a traditional server environment might be
simpler and more cost-effective. The serverless application architecture can be
vendor dependent, and so there is a potential for vendor lock-in, particularly
involving platform capabilities such as authentication, scaling, monitoring, or
configuration management. Because serverless architectures scale up and down in
response to workload, they also sometimes need to start up from zero to serve a
new request. For certain applications, this delay isn’t much of an impact, but
for something like a low-latency financial application, this delay wouldn’t be
acceptable.