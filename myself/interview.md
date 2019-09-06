# 前言

讲讲最近出去，外面都问啥问题了

1. 先说说线程池的参数吧，线程池是怎么根据这些核心参数工作的，你们项目中怎么用的线程池，为什么要这么用。
2. 讲讲重载重写，返回值类型不一样是不是重载呢，两个方法参数分别是 List<Integer> 和 List<String> 是不是重载呢，编译报错吗，还是运行报错？
3. 用两个栈实现一个先进先出的队列，写出伪代码，每次取元素都需要把第一栈倒出来，再倒进去吗，这样是不是效率很低，怎么优化。
4. 讲讲 synchronized 和 Lock 的区别，synchronized 是可重入的吗？下面的伪代码，如果用 10 个线程同时调用有问题吗？为什么不行，我用 volatile 修饰 i 呢？为什么还不行？用 AtomicInteger 呢？

```
Integer i = 1;
synchronized Integer get() {
    return i;
}
synchronized set(Integer n) {
    i = n;
}

func () {
    for (int a = 0 ; a < 10000; a++) {
        set(get()++);
    }
}

```
5. 分布式锁可以怎么做？
6. 讲讲 Java 类加载的过程。
7. HashMap 是线程安全的吗？数据结构是什么样的，你说 8 的时候转换成红黑树，6 的时候变回链表，那 7 的时候呢。扩容的时候是怎么做的，为啥是 2 倍。怎么判断数据应该存在数组的哪个位置。
8. springMVC 和 springboot 有啥区别，springboot 有啥好处，spring 又是做啥的？