(Music) Hi. My name is Kaleigh Bovey, with the IBM Cloud team and today we're
going to be talking about virtualization. As you know virtualization is a fairly
old technology, but it's still super relevant to building our cloud computing
strategy today. So, first off, what is virtualization? Simply put,
virtualization is the process of creating a software based, or virtual, version
of something, whether that be compute, storage, networking, servers, or
applications and what makes virtualization feasible, is something called the
hypervisor. We're going to write that here. What a hypervisor is, is it's simply
a piece of software that runs above the physical server, or host. And there are
a couple different types of hypervisors out there.  What they do is essentially
pull the resources from the physical server and allocate them to your virtual
environments. There are two main types of hypervisors out there. One being Type
1. Very simple to remember. And 2, you guessed it, Type 2. So let's start with
Type 1.  A Type 1 hypervisor is a hypervisor that is installed directly on top
of the physical server. They're also called bare-metal hypervisors. So we'll
write that up here. Remember these are the most frequently typed of use
hypervisors and they're most secure, they lower the latency, and these are the
ones that you'll see in the market the most. Some examples would be VMware,
ESXi, or Microsoft Hyper-v, or even open-source KVM. The other type of
hypervisor is a Type 2 hypervisor, over here. And what makes these different is
that there is a layer of host OS that sits between the physical server and the
hypervisor. So, by that nature they are also called, Hosted. These are a lot
less frequent. They're mostly used for end-user virtualization and you might see
some in the market that are called: Oracle, VirtualBox, or VMware Workstation.
Again, they're a lot less frequent. They're a bit more... They have a higher
latency than a Type 1 hypervisor. So once you have your hypervisor installed,
you can build virtual environments, or virtual machines, or simply put, VMs. So
let's spin up some environments. So, what makes a VM a VM? A VM is simply a
software based computer. They're run like a physical computer. They have an
operating system and applications, and they're completely independent of one
another, but you can run multiple of them on a hypervisor and the hypervisor
manages the resources that are allocated to these virtual environments from the
physical server. So, because they're independent you can run different operating
systems on different virtual machines. You could run Windows here, or Linux
here, or UNIX here for example. Because they're independent they're also
extremely portable. You can move a virtual machine from one hypervisor to
another hypervisor on a completely different machine almost instantaneously,
which gives you a lot of flexibility and a lot of portability within your
environment. So looking at all of this - this is the core virtualization as a
process. So let's talk about a couple key benefits that you want to take away
from this. 1) Cost savings. When you think about this and the fact that you can
run multiple virtual environments from one piece of infrastructure, means that
you can drastically reduce your physical infrastructure footprint. This is
consolidation at its core. And the fact that you don't have to maintain nearly
as many servers, run as much electricity, save on maintenance costs, means that
you save on your bottom line at the end of the day. 2) Would be agility and
speed. Like I said, spinning up a virtual machine is relatively easy and quick -
a lot more simple than provisioning an entire new environment for your
developers if they say they want to spin up a new environment so that they can
run a test scenario. Whatever it might be, virtualization makes that process a
lot simpler and quicker and 3) lowers your downtime. So, let's say that this
host goes out unexpectedly. The fact that you can move virtual machines from one
hypervisor to another, on a different physical server, means that you have a
great backup plan in place right? So, if this host goes down you can simply move
your VMs very quickly to another hypervisor on a machine that is working.
Virtualization and VMs are at the center of cloud computing and provide many
benefits. In the next video, we will discuss the types of virtual machines.