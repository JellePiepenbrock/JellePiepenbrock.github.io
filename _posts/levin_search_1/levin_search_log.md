
<details open="open"><summary><em>k=1</em></summary>
<p>

- Initially, $$k = 1$$
- All programs of length $$k = 1$$ are initialized. Given our primitive set there is only one primitive that is of length 1 (i.e. has no arguments): primitive 3, the STOP operation.
- Each program runs until a halt or error occurs
```
Program -> Status after run (Allocated runtime)
[3] -> STOP (512)
```
- The specific program with tape [3] is ran for one step, then halts. 
 The weights do not satisfy ALL training examples, hence we continue to the next program.
- There are no next programs to evaluate, we increase k.


</p>
</details>

<details open="open"><summary><em>k=2</em></summary>
<p>

- All programs of length $$k = 2$$ are initialized. 
 In the general case these consist of instructions with length 2 (i.e. primitives with one argument) and programs composed of a prefix of length one and an instruction of length 1.
 Given our current set of primitives, there are no sensible prefixes ([3 3] is not valid).
- Programs that are obviously syntactically invalid aren't generated. For each primitive, we choose to specific an allowed range of arguments. For example [7 0] is invalid (allocate 0 cells) as is [8 1] (increase a non-writeable cell). 
- Each of the generated programs is ran until it halts, then is evaluated. 
```
Program -> Status after run (Allocated runtime)
[1, 0] -> CONTINUE (512)
[1, 1] -> CONTINUE (512)
[2, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[2, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[2, 2] -> CONTINUE (512)
[7, 1] -> CONTINUE (512)
```
- None of the solutions generate weights that satisfy ALL training samples.
- There are no programs left to evaluate, we increase k.


</p>
</details>

<details><summary><em>k=3</em></summary>
<p>

```
Program -> Status after run (Allocated runtime)
[1, 0] -> CONTINUE (1024)
[1, 0, 3] -> STOP (512)
[1, 1] -> CONTINUE (1024)
[1, 1, 3] -> STOP (512)
[2, 0] -> ERROR_CURRENT_TIME_LIMIT (1024)
[2, 2] -> CONTINUE (1024)
[2, 2, 3] -> STOP (512)
[7, 1] -> CONTINUE (1024)
[7, 1, 3] -> STOP (512)
```

</p>
</details>

<details open="open"><summary><em>k=4</em></summary>
<p>

- All programs of length $$k = 4$$ are initialized. 
- Each of the generated programs is ran until it halts, then is evaluated. 
```
[1, 0] -> CONTINUE (2048)
[1, 0, 1, 0] -> CONTINUE (512)
[1, 0, 1, 1] -> CONTINUE (512)
[1, 0, 1, 2] -> CONTINUE (512)
[1, 0, 1, 3] -> CONTINUE (512)
[1, 0, 2, 0] -> ERROR_WEIGHT_POINTER_OUT_BOUNDS (512)
[1, 0, 2, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[1, 0, 2, 2] -> ERROR_CURRENT_TIME_LIMIT (512)
[1, 0, 2, 3] -> STOP (512)
[1, 0, 2, 4] -> CONTINUE (512)
[1, 0, 7, 1] -> CONTINUE (512)
[1, 1] -> CONTINUE (2048)
[1, 1, 1, 0] -> CONTINUE (512)
[1, 1, 1, 1] -> CONTINUE (512)
[1, 1, 1, 2] -> CONTINUE (512)
[1, 1, 1, 3] -> CONTINUE (512)
[1, 1, 2, 0] -> ERROR_WEIGHT_POINTER_OUT_BOUNDS (512)
[1, 1, 2, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[1, 1, 2, 2] -> ERROR_CURRENT_TIME_LIMIT (512)
[1, 1, 2, 3] -> STOP (512)
[1, 1, 2, 4] -> CONTINUE (512)
[1, 1, 7, 1] -> CONTINUE (512)
[2, 0] -> ERROR_CURRENT_TIME_LIMIT (2048)
[2, 2] -> CONTINUE (2048)
[2, 2, 1, 0] -> CONTINUE (512)
[2, 2, 1, 1] -> CONTINUE (512)
[2, 2, 1, 2] -> CONTINUE (512)
[2, 2, 1, 3] -> CONTINUE (512)
[2, 2, 2, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[2, 2, 2, 1] -> ERROR_CURRENT_TIME_LIMIT (512)
[2, 2, 2, 2] -> ERROR_CURRENT_TIME_LIMIT (512)
[2, 2, 2, 3] -> STOP (512)
[2, 2, 2, 4] -> CONTINUE (512)
[2, 2, 7, 1] -> CONTINUE (512)
[7, 1] -> CONTINUE (2048)
[7, 1, 1, -1] -> CONTINUE (512)
[7, 1, 1, 0] -> CONTINUE (512)
[7, 1, 1, 1] -> CONTINUE (512)
[7, 1, 1, 2] -> CONTINUE (512)
[7, 1, 1, 3] -> CONTINUE (512)
[7, 1, 2, -1] -> ERROR_ILLEGAL_READ (512)
[7, 1, 2, 0] -> ERROR_ALLOCATE_OUT_BOUNDS (512)
[7, 1, 2, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[7, 1, 2, 2] -> ERROR_CURRENT_TIME_LIMIT (512)
[7, 1, 2, 3] -> STOP (512)
[7, 1, 2, 4] -> CONTINUE (512)
[7, 1, 8, -1] -> CONTINUE (512)
[7, 1, 9, -1] -> CONTINUE (512)
[7, 1, 12, 1] -> CONTINUE (512)
[0, 0, 0, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 0, 0, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 0, 0, 2] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 0, 0, 3] -> STOP (512)
[0, 0, 0, 4] -> CONTINUE (512)
[0, 0, 1, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 0, 1, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 0, 1, 2] -> CONTINUE (512)
[0, 0, 1, 3] -> STOP (512)
[0, 0, 1, 4] -> CONTINUE (512)
[0, 0, 2, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 0, 2, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 0, 2, 2] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 0, 2, 3] -> STOP (512)
[0, 0, 2, 4] -> CONTINUE (512)
[0, 0, 3, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 0, 3, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 0, 3, 2] -> STOP (512)
[0, 0, 3, 3] -> STOP (512)
[0, 0, 3, 4] -> CONTINUE (512)
[0, 1, 0, 0] -> CONTINUE (512)
[0, 1, 0, 1] -> CONTINUE (512)
[0, 1, 0, 2] -> CONTINUE (512)
[0, 1, 0, 3] -> CONTINUE (512)
[0, 1, 0, 4] -> CONTINUE (512)
[0, 1, 1, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 1, 1, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 1, 1, 2] -> CONTINUE (512)
[0, 1, 1, 3] -> STOP (512)
[0, 1, 1, 4] -> CONTINUE (512)
[0, 1, 2, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 1, 2, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 1, 2, 2] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 1, 2, 3] -> STOP (512)
[0, 1, 2, 4] -> CONTINUE (512)
[0, 1, 3, 0] -> CONTINUE (512)
[0, 1, 3, 1] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 1, 3, 2] -> STOP (512)
[0, 1, 3, 3] -> STOP (512)
[0, 1, 3, 4] -> CONTINUE (512)
[0, 2, 0, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 2, 0, 1] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 2, 0, 2] -> ERROR_INVALID_INSTRUCTION_POINTER (512)
[0, 2, 0, 3] -> STOP (512)
[0, 2, 0, 4] -> CONTINUE (512)
[0, 2, 1, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 2, 1, 1] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 2, 1, 2] -> CONTINUE (512)
[0, 2, 1, 3] -> STOP (512)
[0, 2, 1, 4] -> CONTINUE (512)
[0, 2, 2, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 2, 2, 1] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 2, 2, 2] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 2, 2, 3] -> STOP (512)
[0, 2, 2, 4] -> CONTINUE (512)
[0, 2, 3, 0] -> CONTINUE (512)
[0, 2, 3, 1] -> CONTINUE (512)
[0, 2, 3, 2] -> CONTINUE (512)
[0, 2, 3, 3] -> STOP (512)
[0, 2, 3, 4] -> CONTINUE (512)
[0, 3, 0, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 3, 0, 1] -> CONTINUE (512)
[0, 3, 0, 2] -> CONTINUE (512)
[0, 3, 0, 3] -> CONTINUE (512)
[0, 3, 0, 4] -> CONTINUE (512)
[0, 3, 1, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 3, 1, 1] -> STOP (512)
[0, 3, 1, 2] -> CONTINUE (512)
[0, 3, 1, 3] -> STOP (512)
[0, 3, 1, 4] -> CONTINUE (512)
[0, 3, 2, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 3, 2, 1] -> STOP (512)
[0, 3, 2, 2] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 3, 2, 3] -> CONTINUE (512)
[0, 3, 2, 4] -> CONTINUE (512)
[0, 3, 3, 0] -> ERROR_CURRENT_TIME_LIMIT (512)
[0, 3, 3, 1] -> STOP (512)
[0, 3, 3, 2] -> STOP (512)
[0, 3, 3, 3] -> STOP (512)
[0, 3, 3, 4] -> CONTINUE (512)
```
- In this phase, two programs satisfy ALL training examples. 
 They generalize perfectly to all other examples.
```
Solutions in this phase [[1, 0, 2, 0], [1, 1, 2, 0]]
```
- We found a solution, so for now we end the search process, however one could obviously continue by increasing _k_ to search for other solutions (for example with a lower number of runtime steps required, but higher Kolmogorov complexity).

</p>
</details>
