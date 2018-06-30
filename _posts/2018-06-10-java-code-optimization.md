---
layout: post
title: "Java Code Optimization"
description: Java 代码优化
image: '/assets/img/placeholder.png'
category: 'blog'
tags:
- java
- optimization
twitter_text: Java 代码优化
introduction: Java 代码优化
---

# Java代码优化

------

 - 应用层
    - 分清使用场合: 最常见的`String`与`StringBuilder`，还有很多。
        - 避免在循环条件中使用复杂表达式
            ```java
            // Bad
            import java.util.Vector;
            class CEL {
                void method (Vector vector) {
                    for (int i = 0; i < vector.size (); i++)  // Violation
                        ; // ...
                }
            }

            // Nice
            class CEL_fixed {
                void method (Vector vector) {
                    int size = vector.size ()
                    for (int i = 0; i < size; i++)
                        ; // ...
                }
            }
            ```
        - 在finally块中关闭Stream
            ```java
            // Bad
            import java.io.*;
            public class CS {
                public static void main (String args[]) {
                    CS cs = new CS ();
                    cs.method ();
                }
                public void method () {
                    try {
                        FileInputStream fis = new FileInputStream ("CS.java");
                        int count = 0;
                        while (fis.read () != -1)
                            count++;
                        System.out.println (count);
                        fis.close ();
                    } catch (FileNotFoundException e1) {
                    } catch (IOException e2) {
                    }
                }
            }

            // Nice
            import java.io.*;
            public class CS {
                public static void main (String args[]) {
                    CS cs = new CS ();
                    cs.method ();
                }
                public void method () {
                    try {
                        FileInputStream fis = new FileInputStream ("CS.java");
                        int count = 0;
                        while (fis.read () != -1)
                            count++;
                        System.out.println (count);
                    } catch (FileNotFoundException e1) {
                    } catch (IOException e2) {
                    } finally {
                        fis.close ();
                    }
                }
            }
            ```
        - 为'Vectors' 和 'Hashtables'定义初始大小
            ```java
            // Bad
            import java.util.Vector;
            public class DIC {
                public void addObjects (Object[] o) {
                    // if length > 10, Vector needs to expand 
                    for (int i = 0; i< o.length;i++) {    
                        v.add(o);   // capacity before it can add more elements.
                    }
                }
                public Vector v = new Vector();  // no initialCapacity.
            }

            // Nice
            public Vector v = new Vector(20);  
            public Hashtable hash = new Hashtable(10); 
            ```
        - 使用'System.arraycopy ()'代替通过循环复制数组
            ```java
            // Bad
            public class IRB
            {
                void method () {
                    int[] array1 = new int [100];
                    for (int i = 0; i < array1.length; i++) {
                        array1 [i] = i;
                    }
                    int[] array2 = new int [100];
                    for (int i = 0; i < array2.length; i++) {
                        array2 [i] = array1 [i];                 // Violation
                    }
                }
            }

            // Nice
            public class IRB
            {
                void method () {
                    int[] array1 = new int [100];
                    for (int i = 0; i < array1.length; i++) {
                        array1 [i] = i;
                    }
                    int[] array2 = new int [100];
                    System.arraycopy(array1, 0, array2, 0, 100);
                }
            }
            ```
        - 让访问实例变量的getter/setter方法变成”final”
            ```java
            // Bad
            public class UISO {
                public UISO () {}
            }
            class Dog extends UISO {
                void method (Dog dog, UISO u) {
                    Dog d = dog;
                    if (d instanceof UISO) // always true.
                        System.out.println("Dog is a UISO"); 
                    UISO uiso = u;
                    if (uiso instanceof Object) // always true.
                        System.out.println("uiso is an Object"); 
                }
            }

            // Nice
            class Dog extends UISO {
                void method () {
                    Dog d;
                    System.out.println ("Dog is an UISO");
                    System.out.println ("UISO is an UISO");
                }
            }
            ```
        - ... ...
    - HotSpot: 关键函数调优
    - ... ...
 - JVM 层

    - GC: 垃圾回收已经不再是经常性的性能杀手了。大多数代码的性能关键并不在这一块，此处提出仅是记录。有兴趣的可以了解检测GC情况的方法及如何调优。
    - JIT: 除非自主添加的代码过于复杂，否则也不用考虑这一块。有兴趣的了解JIT机制及使用场景。
    - ... ...
