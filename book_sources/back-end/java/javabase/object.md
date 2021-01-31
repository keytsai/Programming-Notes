# Object中的11個方法

>getClass(), hashCode(), equals(), clone(), toString(), finalize(), notify(), notifyAll(), 三個wait()

1. getClass()
`public final native Class<?> getClass();`
2. hashCode()
`public native int hashCode();`
3. equals()
`public boolean equals(Object obj) { return (this == obj);}`
4. clone()
`protected native Object clone() throws CloneNotSupportedException;`
5. toString()
6. finalize()
`protected void finalize() throws Throwable { }`
7. notify()
`public final native void notify();`
8. notifyAll()
`public final native void notifyAll();`
9. wait(long timeout)()
`public final native void wait(long timeout) throws InterruptedException;`
10. wait(long timeout, int nanos)()
11. wait()
`public final void wait() throws InterruptedException { wait(0);}`
