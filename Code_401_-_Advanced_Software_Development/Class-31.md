# Class-31

## References 

https://developer.android.com/training/testing/espresso


## Espresso

```
@Test
public void greeterSaysHello() {
    onView(withId(R.id.name_field)).perform(typeText("Steve"));
    onView(withId(R.id.greet_button)).perform(click());
    onView(withText("Hello Steve!")).check(matches(isDisplayed()));
}
```

the onView() method runs only when the message cue is empty, there are no pending actions. This increases the liklihood that only one action will run at a time. Increasing the effectiveness of the test. 

To set up espresso, check the reference for setup instructions on what three settings that need to be disabled. 

Add the espresso dependencies
```
androidTestImplementation 'androidx.test.espresso:espresso-core:3.1.0'
androidTestImplementation 'androidx.test:runner:1.1.0'
androidTestImplementation 'androidx.test:rules:1.1.0'
```
in android.defaultConfig:

```
testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
```
This is the sample test from the docs:
```
@RunWith(AndroidJUnit4.class)
@LargeTest
public class HelloWorldEspressoTest {

    @Rule
    public ActivityScenarioRule<MainActivity> activityRule =
            new ActivityScenarioRule<>(MainActivity.class);

    @Test
    public void listGoesOverTheFold() {
        onView(withText("Hello world!")).check(matches(isDisplayed()));
    }
}
```

```
The main components of Espresso include the following:

Espresso – Entry point to interactions with views (via onView() and onData()). Also exposes APIs that are not necessarily tied to any view, such as pressBack().
ViewMatchers – A collection of objects that implement the Matcher<? super View> interface. You can pass one or more of these to the onView() method to locate a view within the current view hierarchy.
ViewActions – A collection of ViewAction objects that can be passed to the ViewInteraction.perform() method, such as click().
ViewAssertions – A collection of ViewAssertion objects that can be passed the ViewInteraction.check() method. Most of the time, you will use the matches assertion, which uses a View matcher to assert the state of the currently selected view.

```

Finding a view by its R.id is as simple as calling onView():

```
onView(withId(R.id.my_view));
```


