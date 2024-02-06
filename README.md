# Hi there, I'm Alex 👋🏻

I'm a former English teacher turned perpetual student of Computer Science and Software Engineering.

## What's New?

### Rust and The Terminal

In my most recent project, [maze-tui](https://github.com/agl-alexglopez/maze-tui), I explored how to stretch the capabilities of the terminal to create beautiful visualizations of common maze building and graph searching algorithms. With the help of [ratatui.rs](https://github.com/ratatui-org), I was able to realize my vision of interesting and unique algorithm visualizations in the somewhat constrained environment of the Terminal User Interface. Also, the maintainers for ratatui.rs were very helpful in guiding me towards best practices with their library in the Discussion section of their repository. Go check them out! Check out the rough draft [C++](https://github.com/agl-alexglopez/multithreading-with-mazes) version that started it all.

![demo](/images/demo.gif)

Another project on my radar is the [helix-editor](https://github.com/helix-editor/helix). After using Neovim for a few years, I learned of the helix editor project while starting my Rust learning journey. In fact, when I read that helix based their tui library off of the precursor to [ratatui.rs](https://github.com/ratatui-org), [tui.rs](https://github.com/fdehau/tui-rs), I used my [maze-tui](https://github.com/agl-alexglopez/maze-tui) project as an opportunity to learn what tui development was all about. I'm hooked! I will keep an eye on this project as I continue to use it, looking for opportunities to contribute where I can.

## What's Old?

### Algorithm Exploration

I also enjoy exploring new and challenging algorithms and tweaking their core ideas to apply to new and interesting problems. That is the focus of [dancing-links](https://github.com/agl-alexglopez/dancing-links) and [dancing-links-and-planning-pokemon](https://github.com/agl-alexglopez/dancing-links-and-planning-pokemon). What started as Stanford University assignments regarding recursion, vertex covers, and independent sets, turned into reworking these ideas to solve computationally difficult problems. This led me to connect Donald Knuth's [Dancing Links](https://en.wikipedia.org/wiki/Dancing_Links) algorithm to a wide variety of cover problems, even applying it to a beloved video game from my childhood. These projects are written in C++ and I am currently working on big changes for [dancing-links-and-planning-pokemon](https://github.com/agl-alexglopez/dancing-links-and-planning-pokemon), using this project as an opportunity to learn about the relatively new WebGPU API and the not so new OpenGL.

![defense-links](/images/defense-links.png)

### Low Level Principles

With modern C++ practices and languages such as Rust, the direct management of the heap through `new` and `free` mechanisms is becoming a thing of the past. However, it is always good to know what is happening a few layers beneath our abstractions. I wanted to know more about *how* we can make an allocator flexible, efficient, fast, or any combination of these traits. I implemented eight different heap allocators in C and through the use of programs targeted at understanding their performance characteristics wrote an extensive runtime analysis. Five of these allocators are variations on a Red Black Tree allocator and I recently added Splay Trees to the mix. I chose these implementations as they were just *slightly* beyond my skill level to understand and implement at the time, providing a great opportunity for growth. And, most importantly, I put in place the testing framework and analysis tools for anyone else to explore and have fun implementing their own allocator ideas with this repository. Check out the **[heap-allocator-workshop](https://github.com/agl-alexglopez/heap-allocator-workshop)**!

![rbtree-real](/images/rbtree-real.png)   

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

### The Operating System

By far my favorite learning opportunities from Stanford University have come out of their systems track classes. The course offerings in this track are varied, rigorous, and well organized. Next in this sequence for me is an opportunity to implement a small operating system over the course of a quarter. Here are two experiments that have already been generated from learning about development in an Operating System environment.

- [c-str-view](https://github.com/agl-alexglopez/c-str-view/tree/main)
- [tree-lib](https://github.com/agl-alexglopez/tree-lib)
