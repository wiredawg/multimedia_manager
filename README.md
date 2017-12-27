# Multimedia Manager -- Specification

There are many open source and commercial offerings for multimedia management.
Some require you to tie into a particular ecosystem or to give up your privacy
for analysis and marketing and some just are not that stable.  This is not
another offering hoping to solve those issues. The purpose of this repo is to
provide an application that I can use to learn different development
environments. I have taken an interest in programming and although I do it for
a living, my work does not include the topics which I can apply to making tasks
at home easier. So the goal of this project is to have fun developing skills.

One task that I have been tackling manually for over a decade is proper
management of my photo, video, and music library.  Over time this library has
grown quite large and cumbersome, especially with my use of a full frame DSLR
camera and the convenience of phone camera. I find myself inundated by images
and videos I have personally taken and by numerous Music files ripped from CDs
or purchased from iTunes since the mid 90s. 

So far to suffice I have been able to structure my multimedia library as a
somewhat organized directory tree. This is the most portable (and raw) solution
so I have gotten by on it while relying on assorted viewers across devices/OSes
for this long. But I have a continuing need to develop a solution that allows
me greater functionality and consistency across my devices. Hopefully, I can
eventually achieve this in a way that does not tie me to a particular platform
or gets left behind as technologies progress.

However, the more I think about it. Both of those goals are mostly benign. 

The first, avoid locking into an ecosystem, is unavoidable once you move from
an unmanaged directly-based library to anything managed. This is because the
management tool requires infrastructure. The impact of such ecosystem lock
could be reduced if the tool is implemented according to an open specification.
Such a specification would allow implementation of the management tool from
many different ecosystems. 

The last goal, staying relevant as technologies progress is a different
challenge. This is more subjective than anything. As this project is a learning
activity over a long term, it is inevitable that my interests will change
causing me to want to explore alternative implementations.  Since I seem to
visit this topic at least once a year, any time I have a few days off at home,
I have observed that the tools which are my preference at these times
change every time I do this consideration. In the late-2000s I would have
started with ANSI-C and the various GUI offerings for Linux Windows.  By
the early-2010s I was looking into Python and something more cross
platform. (I see some developers have been more successful at this than
others.  E.g. [`picty`][picty]).  A couple years ago I was
looking into a web based JavaScript approach. And, as of now I am
considering a cross platform native/mobile application using
[Mono][mono_proj] as the core provider with clients at various levels of
coupling. But, the problem of picking a technology is inevitable as
trends change so ofter. So to minimize disruption I must take an approach
which allows evolution of design in such a way that former code does not
become legacy code...


# Functional Requirements

Functional requirements are agnostic of technical approach and can be 
discussed independently. Basic requirements are some sort of import 
process that indexes and caches thumbnails in an internal database and
the ability to organize by specific parameters. Aggregated metric snapshots
would be good for quick review of things like space, space used by 
infrastructure, and media counts.

## Requirement List

This is a convenient list of feature requirement:

\*_This list not complete_

1. Import
   - Index and thumbnail cache

2. Organization
   - Albums
   - Type: Photo, Videos, Music, Movies
   - Creation Date

3. Views
   - By Album
   - Timeline

3. Aggregate Metrics
   - Library Size on Disk
   - Size of Media Only
   - Media Count Total and by Type
   - Plugins Active/Inactive

# High-level Block Diagram

The below diagram depicts an example approach which appears to have 
fairly good cross-platform coverage of the core logic. This only 
addresses device coverage concern but does not take into account the
effectiveness of choses ecosystem for this particular task. That
evaluation is still under consideration.

![High-level Structure][arch_block]

_<center>Figure 1. High-level Application Structure</center>_




<!-- Links -->

[picty]: https://github.com/spillz/picty
[mono_proj]: http://www.mono-project.com/
[electron]: https://electronjs.org/
[arch_block]: ./specs/arch_block.png
