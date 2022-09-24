#  Tower Of Hanoi
Tower of Hanoi is a mathematical puzzle where we have three rods (A=source, B=spare or medium or via , and C=destination) and N disks. Initially, all the disks are stacked in decreasing value of diameter i.e., the smallest disk is placed on the top and they are on rod A. The objective of the puzzle is to move the entire stack to another rod (here considered C), obeying the following simple rules: 
<ol>
<li>Only one disk can be moved among the towers at any given time.</ol>
<li>Only the "top" disk can be removed.</li>
<li>No large disk can sit over a small disk.</li>


## Solving using recursion

**Algorithm:**
<ol>
<li>Move n-1 disks from source to medium or via rod</li>
<li>Move n<sup>th</sup> disk from source to dest</li>
<li>Move n-1 disks from aux to dest</li>
</ol>

**Code:**
```
void TOH(int n,char sour, char via,char des)
{ 
	if(n==1)
	{
		cout<<"Move Disk "<<n<<" from "<<sour<<" to "<<des<<endl;
		return;
	}
	
	TOH(n-1,sour,des,via);
	cout<<"Move Disk "<<n<<" from "<<sour<<" to "<<des<<endl;
	TOH(n-1,via,sour,des);
}
```
 
**Example**

Let n=3 rings and A = source, B = medium or via , C = destination . Then the sequence of function call will be as
<ol>
 <li>TOH(3,A,B,C)
   <ol>
         <li>TOH(2,A,C,B)
           <ol>
                <li>TOH(1,A,B,C)</li>
                <li>TOH(1,C,B,A)</li>
           </Ol>
         </li>
         <li>TOH(2,B,A,C)
            <ol>
                <li>TOH(1,B,C,A)</li>
                <li>TOH(1,A,B,C)</li>
            </ol>
         </li>
    </ol>
 </li>
</ol>

If we arrange this in a tree and vsit in In-order transversal , we will get the solution of problem.