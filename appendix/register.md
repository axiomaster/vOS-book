# x86寄存器汇总

## x86寄存器分类

### 8个通用寄存器

*均为32位。*

- EAX

    累加寄存器(Accumulator Register)。

- EBX

    基地址寄存器(Base Register)。

- ECX

    计数寄存器(Count Register)。

- EDX

    数据寄存器(Data Register)。

- ESI
- EDI

    源/目标索引寄存器(Source/Destination Index Register)

- ESP

    基指针寄存器(Base Pointer Register)

- EBP

    堆栈指针寄存器(Stack Pointer Register)

### 6个段寄存器

*段寄存器均为16位。*

- CS

    指向代码段的段选择符，与EIP寄存器联合构成指令地址。

- DS
- ES
- FS
- GS

    指向数据段。

- SS

    指向栈段的段选择符。

### 5个控制寄存器

*均为32位。*

- CR0

<table style="font-size:10px;text-align:center">
<thead>
<tr>
<th style="background-color:#ccc">31</th><th>30</th>
<th style="background-color:#ccc">29</th><th>28</th>
<th style="background-color:#ccc">27</th><th>26</th>
<th style="background-color:#ccc">25</th><th>24</th>
<th style="background-color:#ccc">23</th><th>22</th>
<th style="background-color:#ccc">21</th><th>20</th>
<th style="background-color:#ccc">19</th><th>18</th>
<th style="background-color:#ccc">17</th><th>16</th>
<th style="background-color:#ccc">15</th><th>14</th>
<th style="background-color:#ccc">13</th><th>12</th>
<th style="background-color:#ccc">11</th><th>10</th>
<th style="background-color:#ccc">9</th><th>8</th>
<th style="background-color:#ccc">7</th><th>6</th>
<th style="background-color:#ccc">5</th><th>4</th>
<th style="background-color:#ccc">3</th><th>2</th>
<th style="background-color:#ccc">1</th><th>0</th>
</tr>
</thead>
<tr>
<td style="background-color:#ccc">PG</td>
<td>CD</td>
<td style="background-color:#ccc">NW</td>
<td colspan="10"></td>
<td style="background-color:#ccc">AM</td>
<td></td>
<td style="background-color:#ccc">WP</td>
<td colspan="10"></td>
<td style="background-color:#ccc">NE</td>
<td>ET</td>
<td style="background-color:#ccc">TS</td>
<td>EM</td>
<td style="background-color:#ccc">MP</td>
<td>PE</td>
</tr>
</table>

- CR1

    未启用。

- CR2

    页故障线性地址寄存器。

- CR3

    存储```页目录表```物理内存基地址，也被称为```PDBR(Page-Directory Base address Register)```。

<table style="font-size:10px;text-align:center">
<tr>
<td style="background-color:#ccc">31</td><td>30</td>
<td style="background-color:#ccc">29</td><td>28</td>
<td style="background-color:#ccc">27</td><td>26</td>
<td style="background-color:#ccc">25</td><td>24</td>
<td style="background-color:#ccc">23</td><td>22</td>
<td style="background-color:#ccc">21</td><td>20</td>
<td style="background-color:#ccc">19</td><td>18</td>
<td style="background-color:#ccc">17</td><td>16</td>
<td style="background-color:#ccc">15</td><td>14</td>
<td style="background-color:#ccc">13</td><td>12</td>
<td style="background-color:#ccc">11</td><td>10</td>
<td style="background-color:#ccc">9</td><td>8</td>
<td style="background-color:#ccc">7</td><td>6</td>
<td style="background-color:#ccc">5</td><td>4</td>
<td style="background-color:#ccc">3</td><td>2</td>
<td style="background-color:#ccc">1</td><td>0</td>
</tr>
<tr>
<td colspan="20">页目录基地址</td>
<td colspan="7" style="background-color:#ccc"></td>
<td>PCD</td>
<td style="background-color:#ccc">PWT</td>
<td colspan="3"></td>
</tr>
</table>

### 1个标志寄存器

- EFLAGS

<table style="font-size:10px;text-align:center">
<tr>
<td style="background-color:#ccc">31</td><td>30</td>
<td style="background-color:#ccc">29</td><td>28</td>
<td style="background-color:#ccc">27</td><td>26</td>
<td style="background-color:#ccc">25</td><td>24</td>
<td style="background-color:#ccc">23</td><td>22</td>
<td style="background-color:#ccc">21</td><td>20</td>
<td style="background-color:#ccc">19</td><td>18</td>
<td style="background-color:#ccc">17</td><td>16</td>
<td style="background-color:#ccc">15</td><td>14</td>
<td style="background-color:#ccc">13</td><td>12</td>
<td style="background-color:#ccc">11</td><td>10</td>
<td style="background-color:#ccc">9</td><td>8</td>
<td style="background-color:#ccc">7</td><td>6</td>
<td style="background-color:#ccc">5</td><td>4</td>
<td style="background-color:#ccc">3</td><td>2</td>
<td style="background-color:#ccc">1</td><td>0</td>
</tr>
<tr>
<td colspan="10" style="background-color:#ccc">保留字段</td>
<td>ID</td>
<td style="background-color:#ccc">VTP</td>
<td>VTF</td>
<td style="background-color:#ccc">AC</td>
<td>VM</td>
<td style="background-color:#ccc">RF</td>
<td></td>
<td style="background-color:#ccc">NT</td>
<td colspan="2">IOPL</td>
<td style="background-color:#ccc">OF</td>
<td>DF</td>
<td style="background-color:#ccc">IF</td>
<td>TF</td>
<td style="background-color:#ccc">SF</td>
<td>ZF</td>
<td style="background-color:#ccc"></td>
<td>AF</td>
<td style="background-color:#ccc"></td>
<td>PF</td>
<td style="background-color:#ccc"></td>
<td>CF</td>
</tr>
</table>

### 4个系统地址寄存器

- GDTR

<table style="font-size:10px;text-align:center">
<tr>
<td style="background-color:#ccc">47</td><td>46</td>
<td style="background-color:#ccc">45</td><td>44</td>
<td style="background-color:#ccc">43</td><td>42</td>
<td style="background-color:#ccc">41</td><td >40</td>
<td style="background-color:#ccc">39</td><td>38</td>
<td style="background-color:#ccc">37</td><td>36</td>
<td style="background-color:#ccc">35</td><td>34</td>
<td style="background-color:#ccc">33</td><td>32</td>
<td style="background-color:#ccc">31</td><td>30</td>
<td style="background-color:#ccc">29</td><td>28</td>
<td style="background-color:#ccc">27</td><td>26</td>
<td style="background-color:#ccc">25</td><td>24</td>
<td style="background-color:#ccc">23</td><td>22</td>
<td style="background-color:#ccc">21</td><td>20</td>
<td style="background-color:#ccc">19</td><td>18</td>
<td style="background-color:#ccc">17</td><td>16</td>
<td style="background-color:#ccc">15</td><td>14</td>
<td style="background-color:#ccc">13</td><td>12</td>
<td style="background-color:#ccc">11</td><td>10</td>
<td style="background-color:#ccc">9</td><td>8</td>
<td style="background-color:#ccc">7</td><td>6</td>
<td style="background-color:#ccc">5</td><td>4</td>
<td style="background-color:#ccc">3</td><td>2</td>
<td style="background-color:#ccc">1</td><td>0</td>
</tr>
<tr>
<td colspan="32" style="background-color:#ccc">32位基地址</td>
<td colspan="16">16位界限</td>
</tr>
</table>

- LDTR

    局部描述符表寄存器。

- IDTR

    中断描述符表寄存器。

- TR

    任务状态段寄存器。

### 8个调试寄存器

- DR0
- DR1
- DR2
- DR3
- DR4
- DR5
- DR6
- DR7

### 其他寄存器

- EIP
- TSC

    时间戳寄存器。

- 浮点寄存器

## 参考资料

- [x86寄存器总结](https://www.cnblogs.com/FrankChen831X/p/10482718.html)
- Orange's 一个操作系统的实现
- 30天自制操作系统
- Linux内核设计的艺术 第2版
