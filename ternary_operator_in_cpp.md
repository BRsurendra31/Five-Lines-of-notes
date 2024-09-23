
## return secLarge != INT_MIN ? secLarge : -1; Explain it 

The expression return secLarge != INT_MIN ? secLarge : -1; is using the ternary operator in C++. Let's break it down:
```cpp
condition ? value_if_true : value_if_false;
```

### Equivalent Code Using if-else:
```cpp
if (secLarge != INT_MIN) {
    return secLarge;  // Return the second largest element
} else {
    return -1;  // No second largest found
}
```