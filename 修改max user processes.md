普通用户java程序报错

java.lang.OutOfMemoryError: unable to create native thread: possibly out of memory or process/resource limits reached

查看ulimit -a

为什么 普通用户下 max user processes 的值只有 4096 呢。那么这个值是从那里控制的呢？

按道理来说 ulimit 的数值都是 通过 /etc/security/limits.conf 来修改的，可是我们已经针对 /etc/security/limits.conf 做了 修改，但是为何 max user processes 的数值会不同呢？

后来我们发现 ulimit 下面 nproc 的数值 原来是通过 /etc/security/limits.d/20-nproc.conf 这里面的文件控制的。 我们查看 /etc/security/limits.d/20-nproc.conf  文件

修改保存即生效。
