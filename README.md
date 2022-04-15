## execpp
Exec cpp code in python3.  
Requires [cppimport](https://github.com/tbenthompson/cppimport) and [robotpy-cppheaderparser](https://github.com/robotpy/robotpy-cppheaderparser).
## Install
```
pip install execpp
```
## Usage Example
```python
from execpp import Cppfile
cpp=Cppfile("your_file_name").compile(r"""

#include<iostream>

struct edge{
  int a,b;
  edge(int x,int y):a(x),b(y){}
};

int add(const edge&x){
  cout<<"Add here!\n";
  return x.a+x.b;
}

""")
e1=cpp.edge(3,10)
print(cpp.add(e1))

# Output
# Add here!
# 13
```

## Warning
- ```template``` not supported
- ```Cppfile``` 的参数必须符合**cpp**的变量命名规范
