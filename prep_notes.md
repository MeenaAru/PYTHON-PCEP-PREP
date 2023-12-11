## Python Characteristics
* Free and Open Source
* Portable can be written on one OS and executed on another OS
* Interpreted- Code is run and executed line by line where as in complied lanuages, the entire code is complied that is converting to machine level code first and then finally its run.
* Dynamic Typed-Data Type of Variable is decided at runtime
* Easy to code
* Pythoni can be used to develop Desktop Application(eg notepad),Web based Applications,Database based Applications, Machine learning Programs, AI based and IOT based applications, Network Application, Data analysis Apps

## Python Execution
* Interactive Shell
* IDLE
* script file (File that has extension .py and the python code in it) execute it from your command prompt saying python3 filepath/filename.py

## Python Identifiers
* Case sensitive
* should begin with aplphabets or _ it cannot begin with any other character.
* The name should consists of only alphabets, _ and numbers
* Reserved words or key words cannot be used

## Reserved words or Key Words
Predifined words in python 
eg  True, False, None, if, else, elif, and, or, not, is, def, List, Array

## Variables
* Variable name should be meaningful
* Same rules as Python identifiers
* variable names can be separated by _

``` del variable name      #this command will delete the variable from the memory ```

## Literals
  Data that is assigned to variables
  
### Types of literals

**String Literals**

String values assigned to variables

Can give the literals inside ' '," ",""" """

For more readability can split the string into multiple lines by adding a \

```
name = "meena" \
       "arumugam"
```
       
If we print the name it will be printed in the same line as ```meenaarumugam```

If we want to print it in separate lines then we need to use """

```
name = """meena
arumugam"""
```

output when printed

```
meena
arumugam
```

**Boolean**

Boolean literals are True and False. T and F in caps

**None**

if we assign None to a variable then the previous value is reset to None(That is the variable does not have any value)

```
a=100
a=None
```
Now the value of is None

**Literal collections**

values for arrays, lists


## Data Types
### Sequence

  **Strings**
  **Escape Characters**
  	  
		```
    s = "Python is \"easy\""
		s = "It\'s my book."
		s = "100 \\ 100" # when u need \ to be printed
		s = "Apple \n Orange" # Will print in separate lines ```
  
  **String Functions**
	
		*len -> len("python")
		*index -> a.index("n",4) will check from 4 index for n character
		*count -> a.count("n",4,5) will check between 4th index and 6th index and get the count of n
		*lower()->a.lower()
		*upper()->a.upper()
		*split()-> a.split(" ")
		
   
  **Tuple (element1,element2,......)**
  
   **Properties**  
   
	* Preserves the order while created
    * Duplicates are allowed
    * Can contain different data types
    * Tuples are Immutable, if a tuple has a list as an element, then that list is mutable for eg a=(1,2,3,[5,5,6]) then a[3][0]=4 is valid and the final tuple will be (1,2,3,[4,5,6])
  
   **Tuple Creation**
   
	 * Empty Tuple -> a=()
	 * Tuple with single element -> a=(1,)  if u create it as a=(1) then a is considered as integer and not Tuple
	 * Tuple without paranthesis -> a=1,2,3
	 * Tuple from a list -> a=tuple(list1)
	 * Nested Tuples-> a=(1,2,(3,4))
	 * Tuple with different data types -> a=(1,'a',3)
	
  **Accessing Tuples**
  
	 * Indexes (negative and positive) -> a[0] (first element) or a[-1] (Last element)
	 * slicing -> print(a[0:10:1]) print(a[10::-1]) will reverse the tuple print(a[0:1000]) will print till the last element if the last element is less than 1000, this statement will not error out.
	 **Packing and Unpacking of Tuple**
	 * packing creating a tuple using a list of variables
				  ``` 
          a=1
			  	b=2
				  c=3
				  tup1=a,b,c
          ```
		  	* unpacking process of creating variables using a tuple
				```
        x,y,x = tup1  #This will assign 1 to x,2 to y and 3 to z
        ```
        
				If there are less no of variables then u will get an value error saying too many values to unpack
		
  **List [element1,element2,....]**
	    Properties of List
			Preserves the order of insertion
			Can contain different data types
			Duplicates are allowed
			Mutable
		List Creation
			empty list -> []
			list of numbers -> a=[1,2,3,4]
			list of strings -> a=["python","is","easy"]
			list of multiple data types -> a=[1,'a',2,'b']
			nested lists -> a=[1,2,[1,2,3]]
			split function on a string will return a list
			using the list function  a=list(range(12,17,2))
			using list comprehensions
				new_list = [i for i in range(20) if i%2 == 0] # will create a list of even numbers
				new_list = [i for i in range(20)] # will create a list of integers from 0 to 19
				new_list = [str(i)+" even" if i%2 == 0 else str(i) + " odd" for i in range(3)] output will be ['0 even','1 odd']
		access elements
			Indexex -> both negative and positive indexes -first element-> a[0]   last element-> a[-1]
			Slice operator -> a[m:n:step]
				m -> start indexe
				n -> up to but not including n index
		Updating Lists
			Adding elements and Updating elements-
				using index to change the value -> a[3] = "hello"  will change the 4 the element
				using slicing operators -> a[3:4] = "hello" this will also change the 4 the element
				using append function -> a.append(200) will add 200 at the end of the list
										 a.append([200,300,200]) this will append this list as a nested list to the end of list a. [1,2,3,4,[200,300,200]]
				using extend function -> a.extend([200,300,200]) this will add all the items in this list to  						the end of list a . [1,2,3,4,200,300,200]
				using insert function -> a.insert(index,element) we specify the index where the new element has to be inserted in the list
			Deleting elements -
				del-> del a[1] or del [1:2] - will delete one element or a range of elements from a list
				remove -> a.remove(5) -will remove the first occurance of the item when there are duplicates.
				pop -> a.pop(1) will remove the element index 1 and  a.pop() will remove the last element
				clear -> a.clear() will remove all elements of the list
		functions for list
			len()- a.len() will print the length of the list
			count - a.count(12) will print the total no of occurence of 12
			index- a.index(12) will print the index of the first occurance of 12
			sort - a.sort() will sort the list a and store it in access
			sorted - sorted(a,reverse=True) sorted(a) - this will either sort it in asc or desc and create a new list, the original list is unchanged
			reverse - a.reverse() will reverse the list and store it in a
		Traversing the list
			while loop
			for loop
			
		operators of list
			concatenation (+) -> a=[1,2,3] b=[4,5,6] c= a+b -> c will be [1,2,3,4,5,6]
			repetition (*) -> d= a*3 -> d will be [1,2,3,1,2,3,1,2,3]
			Comparison operators (== and !=) 
				number of elelments is checked
				they are case sensitive
				order of elements is also checked
			Membership operators (in and not in) print(1 in a) output-> false
  **Sets**
  
   **Properties**
   
		* No Duplicates
		* Set of different data types are allowed
		* Order is not maintained and no index
		* Mutable
		
	**Creating Sets**
   
		* s = {1,2,3,4} if there are duplicates it will remove it.
		* s = {1,2,"python"}
		* s = set({1,2,3})
		* Empty set s = {} will create a dictionary so should use s = set()
		* Set cannot have nested sets and lists inside sets, tuples are allowed as they are immutable.
		
	**Modifying Sets**
   
		* We cannot access elements using index as its an unordered collection
		* add -> a.add(5) can add 1 element at a time.
		* update -> a.update(11,22,33) or a.update(range(20)) will add all these elements to the set
		* copy -> b=a.copy() used to create a new copy of existing set
		* pop -> print(a.pop()) will pop any arbitrary element and print it
		* remove -> a.remove(100) if the element is there it will be removed , if it not there it will error out.
		* discard -> a.discard() if the element is there it will be removed , if it not there it will not error out.
		* clear() -> a.clear() all elements of set will be cleared
		* del s -> will delete the entire set itself.
		
	**Sets Operators**
	
	    * union -> a.union(b) or a | b  Will combine all the elements in bot sets
		* intersection -> a.intersection(b) or a & b Will get the elements common to both sets
		* difference -> a.difference(a) or a - b Will get elments from a which are not in b
		* symetric_difference -> a.symetric_difference(b) or a ^ b Will get all elelments except the common elelments.
		* membership operators (in and not in) -> print(1 in a) or print(1 not in a)
		
		
## Boolean
     
## Dictionary
  
   **Properties**
   
		* Stored as Key value pairs
		* Duplicate Keys are not allowed, Duplicate values are allowable
		* Mutable
	
   **Creating Dictionary**
		
		* Empty Dictionary ``` a = {}```
		* a = {1:"Python",2:"Scala"}
		* a = dict({1:"Python",2:"Scala"})
		
	**Accessing Dictionary**
		
		* print(a[Key]) will print the value for the respective key, if the key is not there it will error out.
		* print(a.get(1)) will print the value of the key, if key is not there it will not error out, it will print None.
		
	**Updating Dictionary**
	
		* update for a key
		```
		a[1] = "Java"
		```
		
		If the key is not there it will add it as a new element.
		
	**Dictionary Functions**

		* pop(key) -> a.pop(1) the key 1 and its value will be removed, if the key is not there it will error out.
		* popitem() -> this will remove any 1 arbitrary item from the dictionary
		* del a[2] -> will delete key 2 and its value. del a will delete entire dictionary.
		* a.clear() -> will clear all the elements from the dictionary and not delete the dictionary itself.
		
	**Dictionary Operators**

        * print(<key> in a) -> will check only if keys are in a dictionary
		* print(<key> not in a) -> will check if key is not in dictionary
		
	**Iterate Dictionary**
	
		*  for i,j in a.items(): print (i,j)
		*  for i in a: print(a[i])
	
	**Functions for Dictionary**
	
		* len -> len(a)
		* get(<key>,<default value>) -> a.get(1, "WEB") if the key is not there it will take the default value is specified otherwise return None.
		* keys -> a.keys() can convert it to list list(a.keys())
		* values -> a.values() can convert it to list list(a.values())
		* items -> a.items() can convert it to list list(a.iems()) this will have a list of tuples of key and value.	
		
## Number
	Integer
		Doesn't have any size limit
	Complex
	  Denoted with j
	  has a real part and an imaginary part
	  1+2j
	  1 is real and 2j is imaginary
	Float

Operator Precedence
*************************************************************************************************************
expressions are evaluated from left to right when it contains operators of equal precedence.It takes a left sideed in binding in that case except **
Otherwise the below order is taken while evaluating the expression

Brackets ()
slicing
** ( if the expression has more than 1 of this operator it takes a right sided binding)
sign(+,-), Bitwise complement or bitwise NOT(~)
* / // %
+ -
Bitwise shifts << >> 
Bitwise &(and) 
Bitwise |(or) 
Bitwise ^(xor)
comparison operators  >= > <= < == != in not in is not is
Boolean operator NOT
Boolean operator AND
Boolean operator OR
Conditional expression if ele
Lambda expression lambda
	
Print
*************************************************************************************************************
sep and end
sep default is " "
end default is "\n"

to substitue values in the middle of the sentence that needs to be printed we can use the format function

print("I love {} and {}".format("apples","oranges"))

Or use indexes or names
print("I love {1} and {0}".format("apples","oranges"))
print("I love {a} and {b}".format(a="apples",b="oranges"))

Or use f-strings
a,b="apples","oranges"
print(f"I love {a} and {b}")

To format floats

y = 43.22222
print(f'value is {y:.2f}')
print('value is %.2f' % y)
print('value is {:.2f}'.format(y))


Flow statements
*************************************************************************************************************

control flow statements
	if
	else
	elif
transfer flow statements
	break
	continue
	pass
iterative flow statements
	while
	for 

Functions
*************************************************************************************************************
required arguments
positional arguments
keyword arguments
default arguments
variable length arguments
