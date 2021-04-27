# Class 27

## References 

https://developer.android.com/guide/components/activities/tasks-and-back-stack

https://developer.android.com/training/data-storage/shared-preferences

## Understand Tasks and Back Stack

A task - collection of activities that users interact with when performing a certain job. 

These activities are arranged in a stack.. The Back Stack

"Activities in the stack are never rearranged, only pushed and popped from the stack—pushed onto the stack when started by the current activity and popped off when the user leaves it using the Back button"

### Managing Tasks

```
with attributes in the <activity> manifest element and with flags in the intent that you pass to startActivity().

In this regard, the principal <activity> attributes you can use are:

taskAffinity
launchMode
allowTaskReparenting
clearTaskOnLaunch
alwaysRetainTaskState
finishOnTaskLaunch
And the principal intent flags you can use are:

FLAG_ACTIVITY_NEW_TASK
FLAG_ACTIVITY_CLEAR_TOP
FLAG_ACTIVITY_SINGLE_TOP

```

#### Launch Modes

You can define different launch modes in two ways: 
1. Using the manifest file
2. using intent flags

#### Handling affinities

"The affinity indicates which task an activity prefers to belong to."

"You can modify the affinity for any given activity with the taskAffinity attribute of the <activity> element."

#### Clearing the Back Stack

After a set amount of time the backstack will clear itself other than the root activity. This is becuase if a user does not return to an activity after a while, they are probably returning to complete something new. 


## Save Key Value Data

using SharedPreferences API to save a relatively small amount of key value pairs. 

### get a handle to shared preferences

```
getSharedPreferences() — Use this if you need multiple shared preference files identified by name, which you specify with the first parameter. You can call this from any Context in your app.
getPreferences() — Use this from an Activity if you need to use only one shared preference file for the activity. Because this retrieves a default shared preference file that belongs to the activity, you don't need to supply a name.
```

### write to shared preferences

```
o write to a shared preferences file, create a SharedPreferences.Editor by calling edit() on your SharedPreferences.
```




