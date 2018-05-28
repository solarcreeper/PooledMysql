# Python中_,__,__xx__的区别  
## _xx单下划线开头  
Python中没有真正的私有属性或方法,可以在你想声明为私有的方法和属性前加上单下划线,以提示该属性和方法不应在外部调用.如果真的调用了也不会出错,但不符合规范.
## __xx双下划线开头
双下划线开头,是为了不让子类重写该属性方法.通过类的实例化时自动转换,在类中的双下划线开头的属性方法前加上”_类名”实现.  
## __xx__
此种写法为Python内建属性方法，最好不要在外部调用

## Python之父Guido推荐的规范
| Type                      | Public                | Internal              |
| ------------------------- | --------------------- | ---------             |
| Modules                   |lower_with_under       | _lower_with_under     |
| Packages                  | lower_with_under      |                       |
| Classes                   | CapWords              | _CapWords             |
| Exceptions                | CapWords              |                       |
| Functions                 | lower_with_under()    | _lower_with_under()   |
| Global/Class Constants    | CAPS_WITH_UNDER       | _CAPS_WITH_UNDERG     |
| lobal/Class Variables     | lower_with_under      | _lower_with_under     |
| Instance Variables        | lower_with_under      | _lower_with_under ( protected) or __lower_with_under (private)|
| Method Names              | lower_with_under()    | _lower_with_under() (protected) or __lower_with_under() (private) |
| Function/Method Parameters| lower_with_under      |                       |
| Local Variables           | lower_with_under      |                       |