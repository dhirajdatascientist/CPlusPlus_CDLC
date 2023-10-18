## Pointers(L1)

* Pointers in C++ are a fundamental concept that deals with memory addresses directly. They're a powerful feature, but can also be a source of confusion and bugs if not used carefully. Let's start with the basics:

## What is a Pointer?

A pointer is a variable that holds the memory address of another variable. 

## Declaration

A pointer is declared by specifying the type of the data it points to, followed by an asterisk (`*`), followed by the pointer name.

```cpp
int *ptr;
```

This declares a pointer named `ptr` that can point to an integer.

## Initialization

A pointer can be initialized by assigning it the address of a variable. The address-of operator `&` is used to get the address of a variable.

```cpp
int num = 10;
int *ptr = &num;
```

Now, `ptr` holds the address of `num`.

## Dereferencing

Dereferencing is the act of getting or setting the value that the pointer is pointing to. This is done using the `*` operator.

```cpp
*ptr = 20;  // sets the value at the address ptr is pointing to, i.e., num, to 20
```

Now, `num` would be `20`.

## Pointer Arithmetic

Pointers can be incremented or decremented, and this is especially useful when dealing with arrays.

```cpp
int arr[3] = {10, 20, 30};
int *ptr = arr; // Pointing to the first element

*ptr;       // 10, as ptr points to arr[0]
*(ptr + 1); // 20, as ptr+1 points to arr[1]
*(ptr + 2); // 30, as ptr+2 points to arr[2]
```

## Null Pointer

A pointer that does not point to any valid location is called a NULL pointer. It's a good practice to initialize pointers to `nullptr` (in C++11 and later) if they aren't assigned to any valid memory address initially.

```cpp
int *ptr = nullptr;
```

## Pointer to Pointer

You can also have pointers that point to other pointers.

```cpp
int num = 10;
int *ptr1 = &num;  // pointer to int
int **ptr2 = &ptr1; // pointer to a pointer to int
```

## Common Pitfalls

1. **Dangling Pointers**: This happens when a pointer is pointing to a memory location that has been freed or deleted. Dereferencing such a pointer can lead to undefined behavior.

2. **Memory Leaks**: If you allocate memory using `new` (or `malloc` in C) and fail to deallocate it using `delete` (or `free` in C), you cause a memory leak.

3. **Array Overruns/Underruns**: This happens when you access memory outside the bounds of an array using pointer arithmetic.

4. **Uninitialized Pointers**: Dereferencing an uninitialized pointer can also lead to undefined behavior.

## Dynamic Memory Allocation

In C++, we can allocate memory dynamically using `new` and deallocate using `delete`.

```cpp
int *p = new int;  // Allocates an integer in memory and returns its address to p
*p = 10;  // Assigns 10 to the newly allocated memory

delete p;  // Frees the memory
```
