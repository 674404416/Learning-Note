# C++ Const的三种用法

### 1.概括

**左定值，右定向，const修饰不变量**

### 2.左定值

修饰指针指向的内容

```c++
int a=2;
const int *p=&a;//p的值不可以变，但是p的地址没有固定，可以变地址

int a = 2;
int const *p = &a;//也是左定值，应该是根据const是在*（指针）的左右来判断的

//这是可以的
int a = 2;
const int *p = &a;
cout << *p << endl;
int b = 12;
p = &b;
cout << *p;
```

### 3.右定向



```c++
int a = 2;
int* const p = &a;//p的地址定了，但是p的值没定，可以变

//这是可以的
int a = 2;
int* const p = &a;
cout << *p << endl;
*p = 3;
cout << *p << endl;
```



### 4.双定

```c++
int a = 8;
const int * const  p = &a;//都不能变了
```

