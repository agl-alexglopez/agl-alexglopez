# Hi there, I'm Alex 👋🏻

I'm a former English teacher turned perpetual student of Computer Science and Software Engineering.

## What's New?

### The Operating System

I recently finished implementing the well-known [PintOS](https://www.scs.stanford.edu/24wi-cs212/labs/project.html) kernel and operating system in C. This was a fun and challenging endeavor, especially with some of Stanford University's unique requirements in implementation through the CS212 course offering. From this work I have found a new interest in developing low level libraries to make systems programming easier and more pleasant. These projects started as extensions to the base operating system provided libraries and have developed into libraries under active development.

- [`str_view`](https://github.com/agl-alexglopez/str_view) - A string helper library providing read only string handling, searching, and tokenization in C (now available through [vcpkg](https://github.com/microsoft/vcpkg)).
- [`C Container Collection (ccc)`](https://github.com/agl-alexglopez/ccc) - A collection of containers written in C with a focus on memory flexibility and programmer control.

## What's Old?

### Rust and The Terminal

In [maze-tui](https://github.com/agl-alexglopez/maze-tui), I explored how to stretch the capabilities of the terminal to create beautiful visualizations of common maze building and graph searching algorithms. With the help of [ratatui.rs](https://github.com/ratatui-org), I was able to realize my vision of interesting and unique algorithm visualizations in the somewhat constrained environment of the Terminal User Interface. Also, the maintainers for ratatui.rs were very helpful in guiding me towards best practices with their library in the Discussion section of their repository. Go check them out! Check out the rough draft [C++](https://github.com/agl-alexglopez/multithreading-with-mazes) version that started it all.

![demo](/images/demo.gif)

### Algorithm Exploration

I also enjoy exploring new and challenging algorithms and tweaking their core ideas to apply to new and interesting problems. That is the focus of [dancing-links](https://github.com/agl-alexglopez/dancing-links) and [dancing-links-and-planning-pokemon](https://github.com/agl-alexglopez/dancing-links-and-planning-pokemon). What started as Stanford University assignments regarding recursion, vertex covers, and independent sets, turned into reworking these ideas to solve computationally difficult problems. This led me to connect Donald Knuth's [Dancing Links](https://en.wikipedia.org/wiki/Dancing_Links) algorithm to a wide variety of cover problems, even applying it to a beloved video game from my childhood. These projects are written in C++ and I am currently working on big changes for [dancing-links-and-planning-pokemon](https://github.com/agl-alexglopez/dancing-links-and-planning-pokemon), using this project as an opportunity to learn about the relatively new WebGPU API and the not so new OpenGL.

![defense-links](/images/defense-links.png) 

## What's Next?

### Compilers

The black box of compilers has always been fascinating to my and I will finally have a chance to build a compiler, opening the box!
