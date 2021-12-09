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
        <div class="cell cell--6"><div><img src="https://gitee.com/bedoom/images/raw/master/202112091626096.png" alt="image-20211209162623129"  /></div></div>   
        <div class="cell cell--6"><div><img src="https://gitee.com/bedoom/images/raw/master/202112091631474.png" alt="image-20211209163059790"  /></div></div>     
    </div>
</div>

**方法一**：写出表达式直接一一对应，是最简单的，但是I don't like。

```vhdl
entity adder4 if
    port(a, b: std_logic_vector(3 downto 0);
        ci: std_logic;
        s: std_logic_vector(3 downto 0);
        co: std_logic);
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

![image-20211209164411678](https://gitee.com/bedoom/images/raw/master/202112091644789.png){:.shadow}



## 时序逻辑设计

