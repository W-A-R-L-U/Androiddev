# Basics of Android development

```
class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            GreetingCardTheme {
                // A surface container using the 'background' color from the theme
                Surface(
                    modifier = Modifier.fillMaxSize(),
                    color = MaterialTheme.colorScheme.background
                ) {
                    Greeting("Android")
                }
            }
        }
    }
}
```
* The **onCreate()** function is the entry point to this Android app and calls other functions to build the user interface. In Kotlin programs, the main() function is the entry point/starting point of execution. In Android apps, the onCreate() function fills that role.
* The **setContent()** function within the **onCreate()** function is used to define your layout through composable functions. All functions marked with the **@Composable** annotation can be called from the **setContent()** function or from other Composable functions. The annotation tells the Kotlin compiler that this function is used by Jetpack Compose to generate the UI.

### Composable functions

<picture>
<img src="https://github.com/W-A-R-L-U/Androiddev/assets/114277372/caf6a19d-f091-4550-a376-75c63377ff4a" width="600" height="200">
</picture>

1 You add the @Composable annotation before the function.<br>
2 @Composable function names are capitalized.<br>
3 @Composable functions can't return anything.

```
@Composable
fun Greeting(name: String, :  = ) {
    Text(
        text = "Hello $name!",
         = 
    )
}
```
* The **@Preview** annotation tells Android Studio that this composable should be shown in the design view of this file.

### Changing background color
* To change the backgroung color **Surface()** is used.  A Surface is a container that represents a section of UI where you can alter the appearance, such as the background color or border.
* Highlight which part you want to add background color and then press alt+enter for windows or option+enter for mac and then select widget and then select container, change the box to **Surface()**

* A **Modifier** is used to augment or decorate a composable. One modifier you can use is the padding modifier, which adds space around the element

## Jetpack Compose
* Jetpack Compose is a modern toolkit for building Android UIs.
### Annotaions 
* Annotations are means of attaching extra information to code. This information helps tools like the Jetpack Compose compiler, and other developers understand the app's code.
* Annotations with parameters
* Annotation without parameters
Eaxmple of annotations are **@Composable** and **@Preview** <br>
* **Scalable pixels** - The scalable pixels (SP) is a unit of measure for the font size.
* UI elements in Android apps use two different units of measurement: density-independent pixels (DP), which you use later for the layout, and scalable pixels (SP). By default, the SP unit is the same size as the DP unit, but it resizes based on the user's preferred text size under phone settings.


* To display the text **Text()** function is called
* Elements in Text() function are: <br>
       text - text to be displayed<br>
       fontSize -  to chnage the font size<br>
       lineHeight - to add vertical space<br>
* A composable function might describe several UI elements. However, if you don't provide guidance on how to arrange them, Compose might arrange the elements in a way that you don't like.

### UI Hierarchy
* The UI hierarchy is based on containment, meaning one component can contain one or more components, and the terms parent and child are sometimes used.
* The three basic elements
  1. Column
  2. Row
  3. Box
  
<picture>
<img src="https://github.com/W-A-R-L-U/Androiddev/assets/114277372/8487cda6-ffc3-463f-8b1e-34ba8add80af" width="250" height="150">
</picture>

* Column, Row, and Box are composable functions that take composable content as arguments, so you can place items inside these layout elements.
* To display an image **Image** composable is used
* **R class** -  An R class is an automatically generated class by Android that contains the IDs of all resources in the project.
* Box layout is one of the standard layout elements in Compose. Use Box layout to stack elements on top of one another. Box layout also lets you configure the specific alignment of the elements that it contains.
* **alpha** is used for opacity of image
* **Padding** - A UI element wraps itself around its content. To prevent it from wrapping too tightly, you can specify the amount of padding on each side.

```
// This is an example.
Modifier.padding(
    start = 16.dp,
    top = 16.dp,
    end = 16.dp,
    bottom = 16.dp
)
```

### Steps to add an image
1. Add the image from loacl computer to the resource in android studio
2. make a variable and assign value returned from the function call **painterReource(id)**, which takes the image location as id
3. Use the Image composable and pass the variable into the **painter** argument

