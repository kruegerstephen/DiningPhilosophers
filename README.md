# DiningPhilosophers

From the Little Book of Semaphores

The Dining Philosophers Problem was proposed by Dijkstra in 1965, when dinosaurs
ruled the earth [3]. It appears in a number of variations, but the standard
features are a table with five plates, five forks (or chopsticks) and a big
bowl of spaghetti. Five philosophers, who represent interacting threads, come
to the table and execute the following loop:

The forks represent resources that the threads have to hold exclusively in
order to make progress. The thing that makes the problem interesting, unrealistic,
and unsanitary, is that the philosophers need two forks to eat, so a hungry
philosopher might have to wait for a neighbor to put down a fork.

Assume that the philosophers have a local variable i that identifies each
philosopher with a value in (0..4). Similarly, the forks are numbered from 0 to
4, so that Philosopher i has fork i on the right and fork i + 1 on the left. Here
is a diagram of the situation:


Assuming that the philosophers know how to think and eat, our job is to
write a version of get forks and put forks that satisfies the following constraints:

• Only one philosopher can hold a fork at a time.

• It must be impossible for a deadlock to occur.

• It must be impossible for a philosopher to starve waiting for a fork.

• It must be possible for more than one philosopher to eat at the same time
