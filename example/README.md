#W3

###任务一：

SteganographyFactory类中的getSteganography()方法接受两个参数，一个是需要编译的源文件，一个是源图片的相对地址，借助SteganographyEncoder类和一些java类将源文件编译后产生的字节码隐写进图片中并将新图片写在根目录下生成隐写图片

运行时，通过自己写的类加载器添加url参数，重写findclass()方法，在调用loadClass()方法使得能够从链接的图片中的字节码中寻找类，创建Class对象，由于事先知道加载类为原本Sorter类型，再将Class对象强制转化为Sorter对象，其余与W2相同。

###任务二：

(图片用的push到github上的链接，经试用发现不能正确找到类，本地运行时使用的是相对链接)

```java
    Geezer theGeezer = Geezer.getTheGeezer();

    SteganographyClassLoader loader = new SteganographyClassLoader(
        new URL("file:example.QuickSort_MJ.png"));

    //SteganographyClassLoader loader = new SteganographyClassLoader(new URL("https://raw.githubusercontent.com/jwork-2021/jw03-2020-qqtcg/main/example.QuickSort_MJ.png"));

    Class c = loader.loadClass("example.QuickSort_MJ");

    Sorter sorter = (Sorter) c.newInstance(); 
```

BubbleSort_MJ():

![](https://raw.githubusercontent.com/jwork-2021/jw03-2020-qqtcg/main/example.BubbleSort_MJ.png)

QuickSort_MJ():

![](https://raw.githubusercontent.com/jwork-2021/jw03-2020-qqtcg/main/example.QuickSort_MJ.png)

###任务三

BubbleSort_MJ()动画:

[![asciicast](https://asciinema.org/a/f5oF3AShKCPQ6GYorHKHPyFct.svg)](https://asciinema.org/a/f5oF3AShKCPQ6GYorHKHPyFct)

QuickSort_MJ()动画:

[![asciicast](https://asciinema.org/a/06kMZRC4sEYDZk0ijdIPT6Y67.svg)](https://asciinema.org/a/06kMZRC4sEYDZk0ijdIPT6Y67)

###任务四

用的练健恒同学的两个图片“example.ShellSorter.png”和“example.QuickSorter.png”（暂时没有链接）

动画（先QuickSorter,后ShellSorter.png）:

[![asciicast](https://asciinema.org/a/8QpBTnawclz9Se0IspEuye2oh.svg)](https://asciinema.org/a/8QpBTnawclz9Se0IspEuye2oh)