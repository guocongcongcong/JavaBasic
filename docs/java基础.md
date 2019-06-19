# Java 基础

<!-- TOC -->

- [Java 基础](#java-基础)
    - [1. JDK 和 JRE 有什么区别？](#1-jdk-和-jre-有什么区别)
    - [2. == 和 equals 的区别是什么？](#2--和-equals-的区别是什么)
    - [3. 两个对象的 hashCode()相同,则 equals()也一定为 true,对吗？](#3-两个对象的-hashcode相同则-equals也一定为-true对吗)
    - [4. final 在 java 中有什么作用？](#4-final-在-java-中有什么作用)
    - [5. java 中的 Math.round(-1.5) 等于多少？](#5-java-中的-mathround-15-等于多少)
    - [6. String 属于基础的数据类型吗？](#6-string-属于基础的数据类型吗)
    - [7. java 中操作字符串都有哪些类？它们之间有什么区别？](#7-java-中操作字符串都有哪些类它们之间有什么区别)
    - [8. String str="i"与 String str=new String(“i”)一样吗？](#8-string-stri与-string-strnew-stringi一样吗)
    - [9. 如何将字符串反转？](#9-如何将字符串反转)
    - [10. String 类的常用方法都有那些？](#10-string-类的常用方法都有那些)
    - [11. 抽象类必须要有抽象方法吗？](#11-抽象类必须要有抽象方法吗)
    - [12. 普通类和抽象类有哪些区别？](#12-普通类和抽象类有哪些区别)
    - [13. 抽象类能使用 final 修饰吗？](#13-抽象类能使用-final-修饰吗)
    - [14. 接口和抽象类有什么区别？](#14-接口和抽象类有什么区别)
    - [15. java 中 IO 流分为几种？](#15-java-中-io-流分为几种)
    - [16. BIO、NIO、AIO 有什么区别？](#16-bionioaio-有什么区别)
    - [17. Files 的常用方法都有哪些？](#17-files-的常用方法都有哪些)
    - [18. java 如何解决的多重继承](#18-java-如何解决的多重继承)

<!-- /TOC -->

## 1. JDK 和 JRE 有什么区别？

- JDK:Java Deveplment Kit--面向开发人员的 SDK.它提供了 JAVA 的开发环境和运行环境

  > SDK:Software Devemplment Kit--软件开发包

- JRE:Java Runtime Enviroment--面向使用者.提供了 JAVA 的运行环境

- JVM:Java virtual machine--是我们常说的 Java 虚拟机

## 2. == 和 equals 的区别是什么？

- ==：比较的是两个字符串内存地址(堆内存)的数值是否相等,属于数值比较；
- equals()：比较的是两个字符串的内容,属于内容比较.

## 3. 两个对象的 hashCode()相同,则 equals()也一定为 true,对吗？

- 对于 Object 类来说,equals()方法在对象上实现的是差别可能性最大的等价关系,即,对于任意非 null 的引用值 x 和 y,当且仅当 x 和 y 引用的是同一个对象,该方法才会返回 true.
- 需要注意的是当 equals()方法被 override 时,hashCode()也要被 override.按照一般 hashCode()方法的实现来说,相等的对象,它们的 hash code 一定相等.
- 并不要求根据 equals(java.lang.Object)方法不相等的两个对象,调用二者各自的 hashCode()方法必须产生不同的 integer 结果.
- Java 对象的 eqauls 方法和 hashCode 方法是这样规定的：
  1.  相等(相同)的对象必须具有相等的哈希码(或者散列码).
  2.  如果两个对象的 hashCode 相同,它们并不一定相同.

## 4. final 在 java 中有什么作用？

- 一旦你将引用声明作 final,你将不能改变这个引用了
- 可以用来生命：可以声明成员变量、方法、类以及本地变量.
- final 关键字提高了性能.JVM 和 Java 应用都会缓存 final 变量.
- final 变量可以安全的在多线程环境下进行共享,而不需要额外的同步开销.
- 使用 final 关键字,JVM 会对方法、变量及类进行优化.

## 5. java 中的 Math.round(-1.5) 等于多少？

- Math.round(11.5)的返回值是 12,Math.round(-11.5)的返回值是-11.四舍五入的原理是在参数上加 0.5 然后进行下取整.
- 规则： 加 0.5,进行下取整;

## 6. String 属于基础的数据类型吗？

- 基础数据类型 8 种：byte、short、int、long、float、double、char、boolean
- String 是对象,是引用类型.

## 7. java 中操作字符串都有哪些类？它们之间有什么区别？

- [链接](https://blog.csdn.net/qq_35246620/article/details/56024465)
- 对于操作效率而言,一般来说,StringBuilder > StringBuffer > String；
- 对于线程安全而言,StringBuffer 是线程安全的,可用于多线程；而 StringBuilder 是非线程安全的,用于单线程；
- 对于频繁的字符串操作而言,无论是 StringBuffer 还是 StringBuilder,都优于 String.
- String: 在 java.lang 下不可被继承的 final 类
- StringBuffer:区别在于修改对象本身,线程安全可以用于多线程
- StringBuilder: 脱胎于 StringBuffer,允许多线程方法添加或者删除,线程不安全,一般用于单线程.

## 8. String str="i"与 String str=new String(“i”)一样吗？

> [答案链接](https://www.cnblogs.com/bluestorm/p/3296897.html)

- String str = "a"; 这个只是一个引用,内存中如果有“a"的话,str 就指向它；如果没有,才创建它;

- 如果你以后还用到"a"这个字符串的话并且是这样:String str1 = "a"; String str2 = "a"; String str2 = "a"; 这 4 个变量都共享一个字符串"a".而 String str = new String("a");是根据"a"这个 String 对象再次构造一个 String 对象,将新构造出来的 String 对象的引用赋给 str.

  > [链接](https://www.cnblogs.com/aspirant/p/9193112.html)

## 9. 如何将字符串反转？

- String reverse = new StringBuffer(string).reverse().toString();

## 10. String 类的常用方法都有那些？

- > [链接](https://www.cnblogs.com/ABook/p/5527341.html)

- public int length()

- public char charAt(int index)

- public String substring(int beginIndex, int endIndex)

- public boolean equals(Object anotherObject)

- public String concat(String str)//"aa"+"bb"+"cc";

- public int indexOf(int ch/String str)

- public String toLowerCase()/public String toUpperCase()

- public String replace(char oldChar, char newChar)

- public String String trim()

- public String[] split(String str)

  ```java
  // 求长度
  // public int length();
  String str = new String("asdfgz");
  int strlength = str.length();        //strlength = 7
  // 求某个字符串的某一位字符
  // public char charAt(int index);
  String str = new String("asdfz");
  char ch = str.charAt(4);             //ch=z
  // 提取子串
  // 1)public String substring(int beginIndex)
  // 2)public String substring(int beginIndex,int endIndex);
  String str1 = new String("asdfgxz");
  Stirng str2 = str1.substring(2);     // str2 = "dfzxc"
  String str3 = str1.substring(2,5);   // str3 = "dfz"
  // 字符串比较
  // 1)public int compareTo(String anotherString);//该方法是对字符串内容按字典顺序进行大小比较,通过返回的整数值指明当前字符串与参数字符串的大小关系.若当前对象比参数大则返回正整数,反之返回负整数,相等返回0.
  // 2)public int compareToIgnore(String anotherString)//与compareTo方法相似,但忽略大小写.
  // 3)public boolean equals(Object anotherObject)//比较当前字符串和参数字符串,在两个字符串相等的时候返回true,否则返回false.
  // 4)public boolean equalsIgnoreCase(String anotherString)//与equals方法相似,但忽略大小写.
  String str1 = new String("abc");
  String str2 = new String("ABC");
  int a = str1.compareTo(str2);//a>0
  int b = str1.compareToIgnoreCase(str2);//b=0
  boolean c = str1.equals(str2);//c=false
  boolean d = str1.equalsIgnoreCase(str2);//d=true
  // 字符串连接
  // public String concat(String str)//将参数中的字符串str连接到当前字符串的后面,效果等价于"+".
  String str = "aa".concat("bb").concat("cc"); //相当于String str = "aa"+"bb"+"cc";
  // 字符串中单个字符查找
  // 1)public int indexOf(int ch/String str)//用于查找当前字符串中字符或子串,返回字符或子串在当前字符串中从左边起首次出现的位置,若没有出现则返回-1.
  // 2)public int indexOf(int ch/String str, int fromIndex)//改方法与第一种类似,区别在于该方法从fromIndex位置向后查找.
  // 3)public int lastIndexOf(int ch/String str)//该方法与第一种类似,区别在于该方法从字符串的末尾位置向前查找.
  // 4)public int lastIndexOf(int ch/String str, int fromIndex)//该方法与第二种方法类似,区别于该方法从fromIndex位置向前查找.
  String str = "I am a good student";
  int a = str.indexOf('a');//a = 2
  int b = str.indexOf("good");//b = 7
  int c = str.indexOf("w",2);//c = -1
  int d = str.lastIndexOf("a");//d = 5
  int e = str.lastIndexOf("a",3);//e = 2
  // 字符串中字符的大小写转换
  // 1)public String toLowerCase()//返回将当前字符串中所有字符转换成小写后的新串
  // 2)public String toUpperCase()//返回将当前字符串中所有字符转换成大写后的新串
  String str = new String("asDF");
  String str1 = str.toLowerCase();//str1 = "asdf"
  String str2 = str.toUpperCase();//str2 = "ASDF"
  // 字符串中字符的替换
  // 1)public String replace(char oldChar, char newChar)//用字符newChar替换当前字符串中所有的oldChar字符,并返回一个新的字符串.
  // 2)public String replaceFirst(String regex, String replacement)//该方法用字符replacement的内容替换当前字符串中遇到的第一个和字符串regex相匹配的子串,应将新的字符串返回.
  // 3)public String replaceAll(String regex, String replacement)//该方法用字符replacement的内容替换当前字符串中遇到的所有和字符串regex相匹配的子串,应将新的字符串返回.
  String str = "asdzxcasd";
  String str1 = str.replace('a','g');//str1 = "gsdzxcgsd"
  String str2 = str.replace("asd","fgh");//str2 = "fghzxcfgh"
  String str3 = str.replaceFirst("asd","fgh");//str3 = "fghzxcasd"
  String str4 = str.replaceAll("asd","fgh");//str4 = "fghzxcfgh"
  ```

## 11. 抽象类必须要有抽象方法吗？

    - 其实这个问题非常明白,用 abstract 修饰的类就是抽象类,并不是说抽象类中必须有抽象方法,即使一个类中的方法全部实现过,也可以用 abstract 修饰为抽象类,所以抽象类不一定都有抽象方法.
    - 延伸：因为真有一种情况可以将类定义为 static 类型的,那就是内部类.

## 12. 普通类和抽象类有哪些区别？

    - 1、普通类可以去实例化调用；抽象类不能被实例化,因为它是存在于一种概念而不非具体.
    - 2、普通类和抽象类都可以被继承,但是抽象类被继承后子类必须重写继承的方法,除非自类也是抽象类.
    - 包含抽象方法的类称为抽象类,但并不意味着抽象类中只能有抽象方法,它和普通类一样,同样可以拥有成员变量和普通的成员方法.注意,抽象类和普通类的主要有三点区别：
      - 1)抽象方法必须为 public 或者 protected(因为如果为 private,则不能被子类继承,子类便无法实现该方法),缺省情况下默认为 public.
      - 2)抽象类不能用来创建对象；
      - 3)如果一个类继承于一个抽象类,则子类必须实现父类的抽象方法.如果子类没有实现父类的抽象方法,则必须将子类也定义为为 abstract 类.
    - 在其他方面,抽象类和普通的类并没有区别

## 13. 抽象类能使用 final 修饰吗？

    - 不能,抽象方法是为了继承之后重写方法的,而用 final 修饰的类,无法继承

## 14. 接口和抽象类有什么区别？

    - > [链接](https://www.jianshu.com/p/038f0b356e9a)
    
    - 抽象类(abstract class):一个抽象类不能实例化,依然可以在类的实体(直白点就是能在｛｝里面)定义成员变量,成员方法,构造方法等.一个类中含有抽象方法(被 abstract 修饰),那么这个类必须被声明为抽象类(被 abstract 修饰).
    
    - 接口(interface):接口在 java 中是一个抽象类型,是抽象方法的集合.一个类通过继承接口的方式,从而继承接口的抽象方法.

## 15. java 中 IO 流分为几种？

    - 两种：输入流与输出流

## 16. BIO、NIO、AIO 有什么区别？

    - IO 的方式通常分为几种，同步阻塞的 BIO、同步非阻塞的 NIO、异步非阻塞的 AIO。
    
    - > [链接](https://blog.csdn.net/skiof007/article/details/52873421)

## 17. Files 的常用方法都有哪些？

    | 方法声明                 | 功能描述                                                     |
    | ------------------------ | ------------------------------------------------------------ |
    | boolean exists()         | 判断 File 对象对应的文件或者目录是否存在若存在则返回 true，否则返回 false |
    | boolean delete()         | 删除 File 对象对应的文件或者目录若成功则返回 true，否则返回 false |
    | boolean createNewFile()  | 当 File 对象对应的文件不存在时，该方法将新建一个此 File 对象所指定的新文件若创建成功则返回 true，否则返回 false |
    | String getName()         | 返回 File 对象表示的文件或文件夹的名称                       |
    | String getPath()         | 返回 File 对象对应的路径                                     |
    | String getAbsolutePath() | 返回 File 对象对应的绝对路径（在 UNIX/Linux 等系统上，如果路径是以正斜线 / 开始的，则这个路径是绝对路径；在 Windows 等系统上，如果路径是从盘符开始的，则这个路径是绝对路径） |
    | String getParent()       | 返回 File 对象对应目录的父目录，（即返回的目录不包含最后一级子目录） |
    | boolean canRead()        | 判断 File 对象对应的文件或者目录是否可读若可读则返回 true，反之返回 false |
    | boolean canWrite()       | 判断 File 对象对应的文件或者目录是否可写。若可写则返回 true，反之返回 false |
    | boolean isFile()         | 判断 File 对象对应的是否是文件（不是目录）若是文件则返回 true，反之返回 false |
    | boolean isDirectory()    | 判断 File 对象对应的是否是目录（不是文件）若是目录则返回 true，反之返回 false |
    | boolean isAbsolute()     | 判断 File 对象对应的文件或者目录是否是绝对路径               |
    | long lastModified()      | 返回 1970 年 1 月 1 日 0 时 0 分 0 秒到文件最好修改时间的毫秒值 |
    | long length()            | 返回文件内容长度                                             |
    | String [ ]list()         | 返回指定目录的全部内容，只列出名称                           |
    | File[ ] listFiles()      | 返回一个包含了 File 对象所有子文件和子目录的 File 数组       |

## 18. java 如何解决的多重继承

    - [链接](https://www.cnblogs.com/chenssy/p/3389027.html) - 1. 接口 - 2. 内部类
