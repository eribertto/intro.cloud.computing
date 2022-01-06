(Music) Containers are an executable unit of software in which application code
is packaged, along with its libraries and dependencies, in common ways so that
it can be run anywhere, whether it be on desktop, traditional IT, or the cloud.
Containers are small, fast, and portable, and unlike virtual machines, they do
not need to include a guest OS in every instance and can, instead, simply
leverage the features and resources of the host OS. In the rest of this video,
we will see how container-based technology really works. Hi everyone. My name is
Sai Vennam and I'm a developer advocate with IBM.Today I want to talk about
containerization. Whenever I mention containers, most people tend to default to
something like Docker or even Kubernetes these days. But container technology
has actually been around for quite some time. It's actually back in 2008 that
the Linux kernel introduced C groups, and control groups, that basically paved
the way for all the different container technologies we see today. So that
includes Docker, but also things like Cloud Foundry, as well as Rocket and other
container runtimes out there. Let's get started with an example, and we'll say
that I was a developer. I've created a node.js application and I want to push it
into production. We'll take two different form factors to kind of explain the
advantages of containerization. Let's say that first we'll talk about VMs, and
then we'll talk about containers. So, first things first, let's introduce some
of the things that we've got here. We've got the hardware itself, just a big
box. We've got the guest, or rather, the host, operating system, as well as a
hypervisor. Hypervisor is actually what allows us to spin up VMs. Let's take a
look at this shared pool of resources with the host OS and hypervisor. We can
assume that some of these resources have already been consumed. Next, let's go
ahead and take this .js application and push it in. And to do that, I need a
Linux VM. So let's go ahead and sketch out that Linux VM. In this VM there's a
few things to note here. So, we've got another operating system, in addition to
the host OS, it's gonna be the guest OS, as well as some binaries and libraries.
That's one of the things about Linux VMs, that even though we're working with a
really lightweight application, to create that Linux VM, we have to put that
guest OS in there, in a set of binaries and libraries. That really bloats it
out. In fact, you know, I think the smallest node .js VM that I've seen out
there is 400 plus mega bytes, whereas the node.js runtime and app itself would
be under 15. So we've got that and we'll go ahead and let's push that .js
application into it. Just by doing that alone, we're gonna consume a set of
resources. Next, let's think about scaling this out. Right. So we'll create two
additional copies of it, and you'll notice that even though it's the exact same
application, we have to use and deploy that separate guest OS and libraries
every time. And so we'll do that three times. And by doing that, essentially, we
can assume that for this particular hardware we've consumed all of the all of
the resources. And there's another thing that I haven't mentioned here, but this
.js application, I developed it on my macbook. So when I pushed it into
production to get it going on the VM, and notice that there were some issues and
incompatibilities. This is the kind of foundations is big, he said, she said
issue. Where things might be working on your local machine, and work great, but
when you try to push it into production, things start to break. and this really
gets in the way of doing agile DevOps, and continuous integration and delivery.
That's solved when you use something like containers. There's a three-step
process when kind of doing anything container related, and then pushing, or
creating, containers. And it almost always starts with first, some sort of a
manifest. So something that describes the container itself. So in the Docker
world, this would be something like a Docker file and in Cloud Foundry, this
would be a manifest Channel. Next, what you'll do is create the actual image
itself. So for the image, again, if you're working with something like Docker,
that could be something like a Docker image. If you're working with Rocket it
would be an ACI or application container image. So regardless of the different
containerization technologies, this process stays the same. The last thing you
end up with is an actual container itself. You know, that contains all of the
runtimes, and libraries, and binaries needed to run an application. That
application runs on a very similar set up to the VMS, but what we've got on this
side is, again, a host operating system. The difference here, instead of a
hypervisor, we're gonna have something like a runtime engine. So if you're using
Docker this would be the Docker engine and, you know, different containerization
technologies would have a different engine. Regardless, it's something that runs
those containers. Again, we've got this shared pool of resources, so we can
assume that that alone consumes some set of resources. Next, let's think about
actually containerizing this technology. We talked about the three-step process.
We create a docker file. We build out the image. We push it to a registry, and
we have our container and we can start pushing this out as containers. The great
thing is, these are going to be much more lightweight. So deploying out multiple
containers, since you don't have to worry about a guest OS this time, you really
just have the libraries, as well as the the application itself. So we've scaled
that out three times, and because we don't have to duplicate all of those
operating system dependencies and create bloated VMs, we actually will use less
resources. So use a different color here... and scaling that out three times, we
still have a good amount of resources left. Next, let's say that my coworker
decides, hey, for this .js application, let's take advantage of a third party
you know  let's say a cognitive API - to do something like image recognition.
Let's say that we've got our third party service, and we want to access that
using maybe a Python application. So he's created that service that acts as that
third party APIs and with our node.js application, we want to access that Python
app, to then access that service. If we wanted to do this in VMs, I'm really
tempted to basically create a VM out of both the .js application and the Python
application because essentially that would allow me to continue to use the VMs
that I have. But that's not truly cloud native, right? Because if I wanted to
scale out the .js, but not the Python app, I wouldn't be able to if they were
running in the same VM. So to do it in a truly cloud native way, essentially I
would have to free up some of these resources. Basically get rid of one of these
VMs, and then deploy the Python application in it instead. And you know, that's
not ideal. But with the container based approach what we can do is simply say,
since we're modular, we can say, okay, just deploy one copy of the Python
application. So we'll go ahead and do that. There's a different color here. And
that consumes a little bit more resources and then with those those remaining
resources, the great thing about container technology, that actually becomes
shared between all the processes running. In fact, another advantage if some of
these container processes aren't actually utilizing the CPU or memory, all of
those shared resources become accessible for the other containers running within
that hardware. So with container-based technology, we can truly take advantage
of cloud native based architectures. We talked about things like portability of
the containers. We talked about how it's easier to scale them out. And then
overall, with this kind of three-step process and the way we push containers,
allows for more agile devops and continuous integration and delivery. Containers
streamline development and deployment of Cloud Native applications. In the next
lesson, we will cover cloud storage.