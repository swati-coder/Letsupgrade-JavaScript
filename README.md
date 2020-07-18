# Letsupgrade-JavaScript Day 1 Assignment
Day1
Q.1
Methods of console function:
1.console.log() method 

console.log('abc');  
console.log(1); 

console.log(true); 

console.log(null); 
console.log(undefined);  

console.log([1, 2, 3, 4]); 

console.log({a:1, b:2, c:3}); 

Output:
abc
1
true 
null
undefined
Array(4) [1,2,3,4]
Object {a: 1,b: 2,c: 3}
>>
2.console error method

console.error('This is a simple error');  
Output:
This is a simple error

3.console warn method
console.warn('This is a warning.'); 
Output:
This is a warning

4.console clear
console.clear();
Output:
Screen cleared

5.console.time() 
6.console.timeEnd() method  

console.time('abc'); 

 let fun =  function(){ 

     console.log('fun is running'); 

 } 

 let fun2 = function(){ 

     console.log('fun2 is running..'); 

 } 

 fun(); // calling fun(); 

 fun2(); // calling fun2(); 

console.timeEnd('abc'); 
Output:
fun is running
fun2 is running..
abc:1ms
>>
7.console.table() method 

console.table({'a':1, 'b':2}); 
Output:
console.table()
(index)
a
b
>>

8.console.count() method 

for(let i=0;i<5;i++){ 

    console.count(i); 
} 
Output:
