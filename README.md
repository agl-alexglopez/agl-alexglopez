# What's Happening?

I'm Alex. Here is what's been happening in my coding life.

## What's New?

### Raylib

I have recently been using [raylib](https://www.raylib.com/) as a tool for modeling interesting problems or learning new concepts. Specifically, I have found it to be a great tool to explore algorithms or spin up a fun application while learning a new programming language.

#### Dancing Links Visualizer

After much consideration, I have finally found raylib to be the perfect tool to visualize Donald Knuth's Dancing Links algorithm for graph cover problems. I have found a fun application of this type of problem solver for the Pokemon video games.

![pokemon-gui](/images/pokemon-gui.png)

Please read my [blog](https://agl-alexglopez.github.io/2025/08/07/the-pok%C3%A9mon-graph-cover-problem.html) post on this topic for more details on how we can model Pokemon type interactions as a graph cover problem. Check out [dancing-links-and-planning-pokemon](https://github.com/agl-alexglopez/dancing-links-and-planning-pokemon) and use the GUI application!

#### Zig

After much consideration, I have decided to explore Zig as the foundation for an educational operating system. Starting with Zig as the build system and gradually incorporating it more into the project, I plan to offer a first class modern developer experience with this language capable of mixing C and Zig. To start, I needed to learn the language. To do so I used my tried and true "[Rosetta Stone](https://agl-alexglopez.github.io/2025/08/01/rosetta-stones-and-mazes-the-premise.html)" program, a maze generator and solver.

![wilson-loop](/images/wilson-loop.gif)

This time, I incorporated isometric pixel art and [raylib-zig](https://github.com/raylib-zig/raylib-zig) in my [iso-mui](https://github.com/agl-alexglopez/iso-mui) project.

### Compilers

I implemented the COOL programming language as part of Stanford's CS143 Compilers course. This was a rewarding experience and I have a greater appreciation for the mix of theoretical and technical complexity that goes into the compilation pipeline. Out of respect for the work the course staff puts in to create their compiler framework the work will remain private for now but I am happy to share on request or discuss the compilation pipeline in detail any time.

## What's Old?

### The Operating System

I recently finished implementing the well-known [PintOS](https://www.scs.stanford.edu/24wi-cs212/labs/project.html) kernel and operating system in C. This was a fun and challenging endeavor, especially with some of Stanford University's unique requirements in implementation through the CS212 course offering. From this work I have found a new interest in developing low level libraries to make systems programming easier and more pleasant. These projects started as extensions to the base operating system provided libraries and have developed into libraries under active development.

- [`str_view`](https://github.com/agl-alexglopez/str_view) - A string helper library providing read only string handling, searching, and tokenization in C (now available through [vcpkg](https://github.com/microsoft/vcpkg)).
- [`C Container Collection (ccc)`](https://github.com/agl-alexglopez/ccc) - A collection of containers written in C with a focus on memory flexibility and programmer control.

## What's Next?

After completing the PintOS projects I have many ideas for how educational operating systems can be improved. Check here for updates on my work towards implementing an operating system scaffolding similar to PintOS or xv6 for learners wanting to enter the field of operating systems. It has begun with my work on the [`C Container Collection (ccc)`](https://github.com/agl-alexglopez/ccc), the data structure framework I hope to have at the core of the OS.

I am also now interested in making this project compatible with both Zig and C. Stay tuned for updates.
