\3. Names representing types must be in mixed case starting with upper case.

3. 代表类型的名字必须首字母大写并且其它字母大小写混合

例如：Line, SavingsAccount



5. Named constants (including enumeration values) must be all uppercase using underscore to separate words.

5. 符号常量(包括枚举值)必须全部大写并用下划线分隔单词

例如：MAX_ITERATIONS, COLOR_RED, PI



26. The prefix is should be used for boolean variables and methods.

26. 布尔变量/函数的命名应使用前缀“is”

例如：isSet, isVisible, isFinished, isFound, isOpen

 

39. The incompleteness of split lines must be made obvious.

39. 断行必须很明显。

在逗号或运算符后换行，新行要对齐



45. Type conversions must always be done explicitly. Never rely on implicit type conversion.

45. 类型转换必须显式声明。永远不要依赖隐式类型转换

例如：floatValue = static_cast<float>(intValue); // NOT: floatValue = intValue;

 Prefer {} initialization over alternatives unless you have a strong reason not to（尽量使用列表初始化，除非你有个很好的不用它的理由）

Why: List initialization does not allow narrowing（原因：列表初始化不允许“窄化”，即不允许丢失数据精度的隐式类型转换）

## 引用的性质（非常重要）

- #### Any changes made through the reference variable are actually performed on the original variable (通过引用所做的读写操作实际上是作用于原变量上).

- #### A reference must be initialized in declaration 引用必须在声明的时候初始化。

- #### Once initialized, the name of the reference cannot be assigned to other variables (引用一旦初始化，引用名字就不能再指定给其它变量)

 