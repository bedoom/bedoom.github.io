---
layout: article
title: "硬件专题复习之逻辑电路设计"
date: 2021-12-09
modify_date: 2021-12-09
author: "Bedoom"
mathjax_autoNumber: false
show_tags: true
tags: 
  - HBU考试内容
---

经过前几次的学习，相信已经是炉火纯青，这章便是试金石，看看是不是一碰就碎。

<!--more-->

## 组合逻辑设计

特点：简单，直接描述真值表即可。

### 设计一个四位加法器

 要求应用一位全加器按如下电路图通过结构描述方式构造四位加法器。

<div class="grid-container"> 
    <div class="grid grid--p-3">   
        <div class="cell cell--6"><div><img src="https://s2.loli.net/2021/12/23/DRof4XxdC6HTPbw.png" alt="image-20211209162623129"  /></div></div>   
        <div class="cell cell--6"><div><img src="https://s2.loli.net/2021/12/23/mRyofbtkVDwBEQH.png" alt="image-20211209163059790"  /></div></div>     
    </div>
</div>
**方法一**：写出表达式直接一一对应，是最简单的，但是I don't like。

```vhdl
entity adder4 if
    port(a, b: in std_logic_vector(3 downto 0);
        ci: in std_logic;
        s: out std_logic_vector(3 downto 0);
        co: out std_logic);
end adder4;
    
ARCHITECTURE rtl OF adder4_3 IS
	COMPONENT full_adder IS
		PORT
		(	a,b,ci		: IN	STD_LOGIC;
			s,co		: OUT	STD_LOGIC		);
	END COMPONENT full_adder;	
	signal C0,C1,C2 : STD_LOGIC;
BEGIN
	u0:full_adder PORT MAP(A(0),B(0),CI,S(0),C0);
	u1:full_adder PORT MAP(A(1),B(1),C0,S(1),C1);
	u2:full_adder PORT MAP(A(2),B(2),C1,S(2),C2);
	u3:full_adder PORT MAP(A(3),B(3),C2,S(3),CO);
END rtl;
```

元件定义：

```vhdl
ENTITY full_adder IS
	PORT
	(a,b,ci: IN	STD_LOGIC;
		s,co: OUT STD_LOGIC);
END full_adder;

ARCHITECTURE rtl OF full_adder IS
BEGIN
	s <= a xor b xor ci;
	co <=  (a and b) or (a and ci) or (b and ci);
END rtl;
```

### 设计一个双向总线缓冲器

![image-20211209164411678](https://s2.loli.net/2021/12/23/9OinFTcxkbNvBg5.png){:.shadow}



## 时序逻辑设计

时序电路的设计会比组合逻辑电路的设计复杂一些，因为时序电路的输出不仅与当前的输入有关，还与以前的输出有关。因此时序电路必然有存储单元，一般为存储器或者寄存器。

1. 直接描述转换真正表
2. 先构造寄存器，然后用RTL描述寄存器之间的逻辑关系
3. 使用结构描述，直接构造电路图

Eg:

要求设计一个具有同步清零和并行输出功能的10进制加法计数器，其引脚名称和逻辑功能如下表所示。

![image-20211212140637456](https://s2.loli.net/2021/12/23/qnm7pTbyEvOZQYr.png){:.shadow}

```vhdl
library ieee;
use ieee.std_logic_1164.all;
use ieee.std_logic_unsignal.all;

entity counter10 is
    port(clk, clr: in std_logic;
        q: buffer std_logic_vector(3 downto 0);
        co: out std_logic);
end counter10;
    
architecture my_function of counter10 is
begin
    process(clk, clr)
    begin
        if(clk'event and clk = '1') then
            if(clr = '0') then
                q<="0000"; co<='0';
        	else
                if(q="1001") then
                    q<="0000"; co<='1';
        		else
                	q <= q+'1'; co <= '0';
        		end if;
            end if;
        end if;
    end process;
end my_function;
```





