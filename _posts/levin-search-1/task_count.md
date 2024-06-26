#### Search process

<table>
<tr>
    <th>Metrics</th>
    <th>Solutions</th>
</tr>
<tr>
<td markdown="1">

- search phase limit: $$4$$
- total runs: $$74$$
- total search time: $$17384$$
- total solutions: $$2$$
- generalizing solutions: $$2$$ ($$1.0$$)

</td>
<td markdown="1">


- [1, 0, 2, 0]

- [1, 1, 2, 0]


</td>
</tr>
</table>

<details><summary>Replication</summary>

<table>
<tr>
<td>Run Deterministic Levin Search</td>
<td markdown="1">
  
```      
python levin_search.py COUNT 4 logs/count/
```
        
</td>
</tr>
</table>

</details>

<br />

#### Solutions

<table>
<tr>
<th>Program</th>
<th>Animation</th>
<th>Interpretation</th>
</tr>
<tr>
<td markdown="1">

[1, 0, 2, 0]

Search:
- Found after: $$9$$
- Steps allocated: $$512$$

Program:
- Steps used: $$201$$
- Program length: $$4$$
- Space probability: $$\frac{1}{74}$$
- Complexity: $$9.303304908059076$$

</td>
<td>

<img alt="Program Animation" src="{{ '/assets/images/levin-search-1/count/animation_1_0_2_0.gif' | relative_url }}" width="400px" />

</td>
<td markdown="1">

| Address | Contents | Interpretation |
|---------|----------|----------------|
| 0       | 1        | OUTPUT         |
| 1       | 0        | address        |
| 2       | 2        | JUMP           |
| 3       | 0        | address        |


</td>
</tr>
</table>

<details><summary>Replication</summary>

<table>
<tr>
<td>Obtain program log</td>
<td markdown="1">
      
```  
python run_program.py string 1,0,2,0 program_1_0_2_0.jsonl
```
        
</td>
</tr>
<tr>
<td>Generate animation</td>
<td markdown="1">
       
```      
python program_convert.py program_1_0_2_0.jsonl animation animation_1_0_2_0.gif
```

</td>
</tr>
<tr>
<td>Generate table</td>
<td markdown="1">
     
```   
python program_convert.py program_1_0_2_0.jsonl table table.md
```

</td>
</tr>
</table>

</details>

<br />    


<table>
<tr>
<th>Program</th>
<th>Animation</th>
<th>Interpretation</th>
</tr>
<tr>
<td markdown="1">

[1, 1, 2, 0]

Search:
- Found after: $$13$$
- Steps allocated: $$512$$

Program:
- Steps used: $$201$$
- Program length: $$4$$
- Space probability: $$\frac{1}{74}$$
- Complexity: $$9.303304908059076$$

</td>
<td>

<img alt="Program Animation" src="{{ '/assets/images/levin-search-1/count/animation_1_1_2_0.gif' | relative_url }}" width="400px" />

</td>
<td markdown="1">

| Address | Contents | Interpretation |
|---------|----------|----------------|
| 0       | 1        | OUTPUT         |
| 1       | 1        | address        |
| 2       | 2        | JUMP           |
| 3       | 0        | address        |


</td>
</tr>
</table>

<details><summary>Replication</summary>

<table>
<tr>
<td>Obtain program log</td>
<td markdown="1">
      
```  
python run_program.py string 1,1,2,0 program_1_1_2_0.jsonl
```
        
</td>
</tr>
<tr>
<td>Generate animation</td>
<td markdown="1">
       
```      
python program_convert.py program_1_1_2_0.jsonl animation animation_1_1_2_0.gif
```

</td>
</tr>
<tr>
<td>Generate table</td>
<td markdown="1">
     
```   
python program_convert.py program_1_1_2_0.jsonl table table.md
```

</td>
</tr>
</table>

</details>
    