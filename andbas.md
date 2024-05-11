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
fun Greeting(name: String, modifier: Modifier = Modifier) {
    Text(
        text = "Hello $name!",
        modifier = modifier
    )
}
```
* The **@Preview** annotation tells Android Studio that this composable should be shown in the design view of this file.

### Changing background color
* To change the backgroung color **Surface()** is used.  A Surface is a container that represents a section of UI where you can alter the appearance, such as the background color or border.
* Highlight which part you want to add background color and then press alt+enter for windows or option+enter for mac and then select widget and then select container, change the box to **Surface()**

* A **Modifier** is used to augment or decorate a composable. One modifier you can use is the padding modifier, which adds space around the element 
