## execpp
Exec cpp code in python3.
Requires [cppimport](https://github.com/tbenthompson/cppimport) and [robotpy-cppheaderparser](https://github.com/robotpy/robotpy-cppheaderparser).
## Install
```
pip install execpp
```
## Usage
```python
from execpp import Cppfile
cpp=Cppfile("your file name").compile("""
struct edge{
  int a,b;
  edge(int x,int y):a(x),b(y){}
}
int add(const edge&x){
  return x.a+x.b;
}
""")
e1=cpp.edge(3,10)
print(cpp.add(e1))
```