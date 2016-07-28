# hashCode 与 equals的区别与联系

## 一、equals方法的作用
- 1、默认情况（没有覆盖equals方法）下equals方法都是调用Object类的equals方法，而Object的equals方法主要用于判断对象的内存地址引用是不是同一个地址（是不是同一个对象）。
- 2 、要是类中覆盖了equals方法，那么就要根据具体的代码来确定equals方法的作用了，覆盖后一般都是通过对象的内容是否相等来判断对象是否相等。

没有覆盖equals方法代码如下：

```Java
public class Student {  
    private int age;  
    private String name;  
      
public Student() {  
}  
public Student(int age, String name) {  
    super();  
    this.age = age;  
    this.name = name;  
}  
public int getAge() {  
    return age;  
}  
public String getName() {  
    return name;  
}  
public void setAge(int age) {  
    this.age = age;  
}  
public void setName(String name) {  
    this.name = name;  
}  
} 
```
测试代码如下：
```
import java.util.HashSet;  
import java.util.LinkedList;  
import java.util.Set;  
  
  
public class EqualsTest {  
    public static void main(String[] args) {  
        LinkedList<Student> list = new LinkedList<Student>();  
        Set<Student> set = new HashSet<Student>();  
        Student stu1  = new Student(3,"张三");  
        Student stu2  = new Student(3,"张三");  
        System.out.println("stu1 == stu2 : "+(stu1 == stu2));  
        System.out.println("stu1.equals(stu2) : "+stu1.equals(stu2));  
        list.add(stu1);  
        list.add(stu2);  
        System.out.println("list size:"+ list.size());  
          
        set.add(stu1);  
        set.add(stu2);  
        System.out.println("set size:"+ set.size());  
    }  
  
}  
```