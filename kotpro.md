# KOTLIN programming

### structure of kotlin 
```
fun main() {
    println("Hello, world!")
}
```

### Data types
* String
* Int
* Double
* Float
* Boolean

### variable declaration
```
val count: Int = 2
```
<picture>
<img src="https://github.com/W-A-R-L-U/kotlin/assets/114277372/747ff234-ce23-4c99-9ddc-0d89e82410cb" width="800" height="200">
</picture>

* val stands for value
* can omit the datatype but initial value should be provided
* to print a variable in middle of a sentence $ is used

```
fun main() {
    val count: Int = 2
    println("The count is $count")
}
```

* val keyword - Use when you expect the variable value will not change.
* var keyword - Use when you expect the variable value can change.
* one cannot change a value declared using val to change the value of a varibale one should use var instead of val
* mathematical operations are similar to c
* comments are same as c programming // for one line /* */ for more than one line

### functions
* To declare a function in kotlin 'fun' keyword is used
<picture>
<img src="https://github.com/W-A-R-L-U/kotlin/assets/114277372/c845f41c-8bcb-47ca-ab04-16335ec69b25" width="500" height="300">
</picture>

* if you do not specify return type it is Unit(void in c,c++,java and None in python)

```
fun func1(name: String): String {
    val na = "Happy $name"
    return na
}
```

* parameters in kotlin are immutable
* **Named arguments** - When you include the parameter name when you call a function, it's called a named argument.

```
println(func1(name = "Hi"))
```

* **Default arguments** - An initial value is assigned to the parameters so while calling one can omit some parameters if needed

