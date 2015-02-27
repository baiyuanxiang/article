#python 判断连续是0 或1 的最大次数  

[python北京周末培训班](https://github.com/pythonpeixun/article/blob/master/beijing_weekend.md )  
[python上海周末培训班 ](https://github.com/pythonpeixun/article/blob/master/shanghai_weekend.md)  
[c语言从入门到精通远程视频培训](https://github.com/pythonpeixun/article/blob/master/c_course.md)  

贴吧上有人问，从终端读入一个整数n，随机一个输入一个0 或1
判断连续是0 或1 的最大次数。如：
输入
0
0
0
1
1
1
1
0
1
0
1在连续输入中，出现4次

	#coding:utf-8
	"""python北京周末培训班 
	https://github.com/pythonpeixun/article/blob/master/beijing_weekend.md 
	python上海周末培训班 
	https://github.com/pythonpeixun/article/blob/master/shanghai_weekend.md 
	咨询:qq:1465376564 黄哥所写
	做这个练习题的思路是：先用一个n次的循环，将0或1添加到一个list中，
	最后用字典来统计出现的连续是0或1的最大次数

	"""

	input_lst = []
	dict_num = {}
	n = int(raw_input("please input n:\n").strip())
	for i in xrange(n):
	    number = int(raw_input("please input number:\n").strip())
	    input_lst.append(number)
	    
	length = len(input_lst)   
	   
	for i, item in enumerate(input_lst):
	    if  0 < i < length:
	        if input_lst[i] == input_lst[i-1]:
	            if item in dict_num:
	                dict_num[item] += 1
	        else:
	                dict_num[item] = 1        
	print input_lst    
	print max(dict_num.values())
	
