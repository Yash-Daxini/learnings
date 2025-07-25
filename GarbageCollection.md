## Garbage Collection

### Garbage Collection in Java

- In JVM (Java virtual machine) memory devided into three areas:
    1. Young Generation
    2. Old Generation
    3. MetaSpace

1. **Young Generation**: It is the area where new objects are created. It is further divided into three areas:

    - Eden Space, Survivor Space 1, Survivor Space 2

    - When an object is created, it is created in Eden Space. When Eden Space is full, garbage collection is performed. The objects that are still in use are moved to Survivor Space. The objects that are not in use are removed.


2. **Old Generation**: It is the area where long-lived objects are stored. In this area collection happens less frequently.

3. **MetaSpace**: It is java specific memory. It stores class metadata, method information, etc.

> [!NOTE] Other languages may implement generational collection differently.

V8 uses two generational system and .NET garbage collector typically uses three generationals (Generation 0, Generation 1, Generation 2).

The most funamental garbage collection algorithm is Mark and Sweep. It is a simple algorithm that works in two phases:
1. Mark: It marks the objects that are reachable.
2. Sweep: It removes the objects that are not marked.

In mark phase it traveses all references starting from the GC root and marks all objects that are reachable. In sweep phase it removes the objects that are not marked.
