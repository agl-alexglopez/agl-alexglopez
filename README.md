# Hi there, I'm Alex 👋🏻

I'm a former English teacher turned perpetual student of Computer Science and Software Engineering.

## What's New?

### The Operating System

I recently finished implementing the well-known [PintOS](https://www.scs.stanford.edu/24wi-cs212/labs/project.html) kernel and operating system. This was a challenging endeavor, especially with some of Stanford University's unique requirements in implementation through the CS212 course offering. From this work I have found a new interest in developing low level libraries to make systems programming easier and more pleasant. These projects started as extensions to the base operating system provided libraries and have developed into libraries under active development.

- [`str_view`](https://github.com/agl-alexglopez/str_view) - A string helper library providing read only string handling, searching, and tokenization in C (now available through [vcpkg](https://github.com/microsoft/vcpkg)).
- [`tree-lib`](https://github.com/agl-alexglopez/tree-lib) - An exploration of different data structures supported by various types of trees. This library will likely expand to encompass a more general suite of data structures with a wide variety of implementations.

## What's Old?

### Rust and The Terminal

In my most recent project, [maze-tui](https://github.com/agl-alexglopez/maze-tui), I explored how to stretch the capabilities of the terminal to create beautiful visualizations of common maze building and graph searching algorithms. With the help of [ratatui.rs](https://github.com/ratatui-org), I was able to realize my vision of interesting and unique algorithm visualizations in the somewhat constrained environment of the Terminal User Interface. Also, the maintainers for ratatui.rs were very helpful in guiding me towards best practices with their library in the Discussion section of their repository. Go check them out! Check out the rough draft [C++](https://github.com/agl-alexglopez/multithreading-with-mazes) version that started it all.

![demo](/images/demo.gif)

Another project on my radar is the [helix-editor](https://github.com/helix-editor/helix). After using Neovim for a few years, I learned of the helix editor project while starting my Rust learning journey. In fact, when I read that helix based their tui library off of the precursor to [ratatui.rs](https://github.com/ratatui-org), [tui.rs](https://github.com/fdehau/tui-rs), I used my [maze-tui](https://github.com/agl-alexglopez/maze-tui) project as an opportunity to learn what tui development was all about. I'm hooked! I will keep an eye on this project as I continue to use it, looking for opportunities to contribute where I can.

### Algorithm Exploration

I also enjoy exploring new and challenging algorithms and tweaking their core ideas to apply to new and interesting problems. That is the focus of [dancing-links](https://github.com/agl-alexglopez/dancing-links) and [dancing-links-and-planning-pokemon](https://github.com/agl-alexglopez/dancing-links-and-planning-pokemon). What started as Stanford University assignments regarding recursion, vertex covers, and independent sets, turned into reworking these ideas to solve computationally difficult problems. This led me to connect Donald Knuth's [Dancing Links](https://en.wikipedia.org/wiki/Dancing_Links) algorithm to a wide variety of cover problems, even applying it to a beloved video game from my childhood. These projects are written in C++ and I am currently working on big changes for [dancing-links-and-planning-pokemon](https://github.com/agl-alexglopez/dancing-links-and-planning-pokemon), using this project as an opportunity to learn about the relatively new WebGPU API and the not so new OpenGL.

![defense-links](/images/defense-links.png) 

### TCP

In the spring of 2023 I implemented a comprehensive version of the TCP Network protocol bottom to top; starting with the byte stream and ending with a peer to peer connection. The implementation and design principles I learned from the CS144 Stanford Networking course were invaluable. I won the end of quarter competition for most performant Reassembler and my combined ByteStream/Reassembler performance was second behind the course staff! Again, Stanford University requests we keep our solution private, but the repository we worked from is [available publicly every year](https://github.com/CS144). Feel free to check it out and I'm happy to share my work upon request. Here is a teaser of a TCPReceiver/Reassembler diagram from my writeup on that section of the course.

```txt
                            \     TCPReceiver
                             \ +-------------------+
                              \|isn=0              |
                  +---+-----+                      |
>>>>>>>>>>>>>>>>>>|844|afdgh+>>>>>>>>>>>v          |
                  +---+-----+           v          |
                            \  |        v          |
                             \ |        v          |
                              \|        v          |
               +-----+------+           v
<<<<<<<<<<<<<<<|ackno|window|<<<<<<<<<<<<<<<<<<<<<<<<<<<
               +-----+------+           v              ^
                               |        v          |   ^
                               +-----   v  --------+   ^
                                        v              ^
                                 +--------+-----+      ^
                                 |844+2^32|afdgh|      ^
             \                   +--------+-----+      ^                       /
              \                         v              ^                      /
               \                        v              ^                     /
                \                                                           /
                 \                                                         /
                  |                                                       |-First Unacceptable Index-1000
                  |                                                       |
                  | Stored Segments-----------------|                     |
                  | Next Index Needed---|           |                     |
                  | Pushed Bytes--|     |           |                     |
Popped----|       |               |     |           |                     |
          |       |               |     |           |                     |
|-----------------|------------------|  |           |                     |
------------------+------------------+  |        |------------------------|
;asdkjf;laskjdls  | f8299fsdoiuosid8 |-[844+2^32] |[896+2^32]-->[940+2^32]|
------------------+------------------+                  8          s
                                                        a          8
                                                        y          l
                                                        8          n

                                                  Reassembler
```

## What's Next?

### Compilers

The black box of compilers has always been fascinating to my and I will finally have a chance to build a compiler, opening the box!
