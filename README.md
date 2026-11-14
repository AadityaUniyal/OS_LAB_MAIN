# Operating Systems Lab

A collection of C programs and exercises for learning operating-systems concepts, organized by lab date. Topics include processes, inter-process communication (IPC), CPU scheduling, and page replacement.

## Repository contents

| Folder | Topics and programs |
| --- | --- |
| [`July31/Class`](./July31/Class/) | Process IDs and parent/child processes ([`first.c`](./July31/Class/first.c), [`q1_pid_ppid.c`](./July31/Class/q1_pid_ppid.c), [`q2_parent_child.c`](./July31/Class/q2_parent_child.c)); waiting and process calculations ([`q3_wait.c`](./July31/Class/q3_wait.c), [`q4_fibonacci_factorial.c`](./July31/Class/q4_fibonacci_factorial.c), [`q5_fibonacci_factorial_sum.c`](./July31/Class/q5_fibonacci_factorial_sum.c)); [exercise prompts](./July31/Class/Questions.md) |
| [`July31/Homework`](./July31/Homework/) | Even/odd output, multiple children, exit status, orphan and zombie process examples; [homework prompts](./July31/Homework/Homework.md) |
| [`Aug7/Class`](./Aug7/Class/) | Child/parent process exercises: [`fibonacci_armstrong_fork.c`](./Aug7/Class/fibonacci_armstrong_fork.c), [`prime_factorial_fork.c`](./Aug7/Class/prime_factorial_fork.c), and [questions](./Aug7/Class/Questions.md) |
| [`Aug17/Class`](./Aug17/Class/) | Child-process array/sum and permutation exercises: [`sum_prime_child.c`](./Aug17/Class/sum_prime_child.c), [`permutation_child.c`](./Aug17/Class/permutation_child.c), and [questions](./Aug17/Class/Questions.md) |
| [`Sep18`](./Sep18/) | [`Prime.c`](./Sep18/Prime.c) checks whether an array's sum is prime; [`input.c`](./Sep18/input.c) demonstrates parent/child file access |
| [`Sep25`](./Sep25/) | Anonymous pipe exercises: [`pipe1.c`](./Sep25/pipe1.c), [`pipe2.c`](./Sep25/pipe2.c) |
| [`OCT23`](./OCT23/) | IPC examples using named pipes ([`fifo_writer.c`](./OCT23/fifo_writer.c), [`fifo_reader.c`](./OCT23/fifo_reader.c)), message queues ([`message_sender.c`](./OCT23/message_sender.c), [`message_receiver.c`](./OCT23/message_receiver.c)), and shared memory ([`shared_writer.c`](./OCT23/shared_writer.c), [`shared_reader.c`](./OCT23/shared_reader.c)) |
| [`OCT30`](./OCT30/) | CPU scheduling ([`fcfs.c`](./OCT30/fcfs.c), [`sjf.c`](./OCT30/sjf.c), [`priority.c`](./OCT30/priority.c)) and page replacement ([`fifopagereplacement.c`](./OCT30/fifopagereplacement.c), [`lru.c`](./OCT30/lru.c)) |

## Build and run

These are standalone programs, each with its own `main` function. Compile one source file at a time with a C compiler:

```sh
gcc -Wall -Wextra OCT30/lru.c -o lru
./lru
```

Replace the source path and output name to build another program. Most examples that use `fork()`, pipes, or System V IPC are intended for Linux. On Windows, use WSL with a Linux distribution.

## Running IPC examples

Run each pair in separate terminals from the same working directory:

- **Named pipe:** Start `fifo_writer` first, then `fifo_reader`.
- **Message queue:** Start `message_sender` first, then `message_receiver`.
- **Shared memory:** Start `shared_writer` first, then `shared_reader`.

The examples use the current working directory to identify IPC resources, so keep both programs in a pair in the same directory while running them.
