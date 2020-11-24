#### ==
```brainfuck
cell 1 == cell 2: requires 5 free cells
output on cell 3
cell 4 and 5 for copying

,>, cell 1 and 2
>>++++++++[<++++++>-]<< output if false
[>>+>+<<<-]>>>[-<<<+>>>]<<< copy cell 2
[<->-]+< calc difference
[>[-]>.<<[->>>>+<<<<]]> if false (and copy difference)
[> + .<[-]] if true (and output change)
>>>[-<<<<+>>>>] put back difference in cell 1
<[-<<+<+>>>]<<< add value of cell 2 to cells 1 and 2
```
copy:
```brainfuck
,>,
>>++++++++[<++++++>-]<<
[>>+>+<<<-]>>>[-<<<+>>>]<<<
[<->-]+<
[>[-]>.<<[->>>>+<<<<]]>
[>+.<[-]]
>>>[-<<<<+>>>>]
<[-<<+<+>>>]<<<
```

#### duplicate
```brainfuck
+++[>+>+<<-]>>[<<+>>-]
```
