# reference
practice about reference(&amp;)
C++中 引用&与取地址&的区别
一个是用来传值的 一个是用来获取首地址的

&(引用)==>出现在变量声明语句中位于变量左边时,表示声明的是引用.
     
例如: int &rf; // 声明一个int型的引用rf.
&(取地址运算符)==>在给变量赋初值时出现在等号右边或在执行语句中作为一元运算符出现时
                  表示取对象的地址.

 

在C++中，既有引用又有取地址，好多人对引用和取地址不是很清楚，因此也无法区分。其实他们的区别可以用一句话概括：和类型在一起的是引用，和变量在一起的是取址。下面我们通过实例具体了解一下

1）引用在赋值=的左边，而取地址在赋值的右边，比如

int a=3；
int &b=a；        //引用
int *p=&a;        //取地址

2）和类型在一起的是引用，和变量在一起的是取址。 举例同样如上，还有下例：
int function(int &i)
 
{
 
}  //引用

3）对于vector，上面2条同样适合
vector<int> vec1(10,1);  //initialize vec1: 10 elements, every element's value is 1
vector<int> &vec2 = vec1; // vec2 is  reference to vec1
vector<int> *vec3 = &vec2; //vec3 is addresss of vec1 and vec2
