**代码案例 :**
``` cpp
#include <iostream>
using namespace std;

class Base {
public:
	void runFunction()
	{
		Function();
	}
private:
	virtual void Function() = 0;
};

class son : public Base {
private:
	void Function()
	{
		cout << "QAQ" << endl;
	}
};

int main()
{
	Base* Temp = new son;
	
	Temp->runFunction();      // 报错:指向绑定函数的指针只能用于调用函数
	
	delete Temp;              // 清理以避免内存泄漏
}
```
