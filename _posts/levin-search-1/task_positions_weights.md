#### Search process

<table>
<tr>
    <th>Metrics</th>
    <th>Solutions</th>
</tr>
<tr>
<td markdown="1">

- search phase limit: $$9$$
- total runs: $$227417$$
- total search time: $$38551962$$
- total solutions: $$2$$
- generalizing solutions: $$2$$ ($$1.0$$)

</td>
<td markdown="1">


- [7, 1, 8, -1, 1, -1, -1, 2, 2]

- [7, 1, 1, -1, -1, 8, -1, 2, 2]


</td>
</tr>
</table>

<details><summary>Replication</summary>

<table>
<tr>
<td>Run Deterministic Levin Search</td>
<td markdown="1">
  
```      
python levin_search.py POSITION 9 logs/position/
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

[7, 1, 8, -1, 1, -1, -1, 2, 2]

Search:
- Found after: $$69349$$
- Steps allocated: $$512$$

Program:
- Steps used: $$303$$
- Program length: $$9$$
- Space probability: $$\frac{1}{227417}$$
- Complexity: $$14.71373280550937$$

</td>
<td markdown="1">

<img alt="Program Animation" src="{{ '/assets/images/levin-search-1/position/animation_7_1_8_-1_1_-1_-1_2_2.gif' | relative_url }}" width="400px" />

</td>
<td markdown="1">

| Address | Contents | Interpretation |
|---------|----------|----------------|
| 0       | 7        | ALLOCATE       |
| 1       | 1        | address        |
| 2       | 8        | INCREMENT      |
| 3       | -1       | address        |
| 4       | 1        | WRITE_WEIGHT   |
| 5       | -1       | address        |
| 6       | -1       | address        |
| 7       | 2        | JUMP           |
| 8       | 2        | address        |


</td>
</tr>
</table>

<details><summary>Replication</summary>

<table>
<tr>
<td>Obtain program log</td>
<td markdown="1">
      
```  
python run_program.py string 7,1,8,-1,1,-1,-1,2,2 program_7_1_8_-1_1_-1_-1_2_2.jsonl
```
        
</td>
</tr>
<tr>
<td>Generate animation</td>
<td markdown="1">
       
```      
python program_convert.py program_7_1_8_-1_1_-1_-1_2_2.jsonl animation animation_7_1_8_-1_1_-1_-1_2_2.gif
```

</td>
</tr>
<tr>
<td>Generate table</td>
<td markdown="1">
     
```   
python program_convert.py program_7_1_8_-1_1_-1_-1_2_2.jsonl table table.md
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

[7, 1, 1, -1, -1, 8, -1, 2, 2]

Search:
- Found after: $$73902$$
- Steps allocated: $$512$$

Program:
- Steps used: $$305$$
- Program length: $$9$$
- Space probability: $$\frac{1}{227417}$$
- Complexity: $$14.720311776607412$$

</td>
<td markdown="1">

<img alt="Program Animation" src="{{ '/assets/images/levin-search-1/position/animation_7_1_1_-1_-1_8_-1_2_2.gif' | relative_url }}" width="400px" />

</td>
<td markdown="1">


| Address | Contents | Interpretation |
|---------|----------|----------------|
| 0       | 7        | ALLOCATE       |
| 1       | 1        | address        |
| 2       | 1        | WRITE_WEIGHT   |
| 3       | -1       | address        |
| 4       | -1       | address        |
| 5       | 8        | INCREMENT      |
| 6       | -1       | address        |
| 7       | 2        | JUMP           |
| 8       | 2        | address        |


</td>
</tr>
</table>

<details><summary>Replication</summary>

<table>
<tr>
<td>Obtain program log</td>
<td markdown="1">
      
```  
python run_program.py string 7,1,1,-1,-1,8,-1,2,2 program_7_1_1_-1_-1_8_-1_2_2.jsonl
```
        
</td>
</tr>
<tr>
<td>Generate animation</td>
<td markdown="1">
       
```      
python program_convert.py program_7_1_1_-1_-1_8_-1_2_2.jsonl animation animation_7_1_1_-1_-1_8_-1_2_2.gif
```

</td>
</tr>
<tr>
<td>Generate table</td>
<td markdown="1">
     
```   
python program_convert.py program_7_1_1_-1_-1_8_-1_2_2.jsonl table table.md
```

</td>
</tr>
</table>

</details>
   
