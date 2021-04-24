# Class 26
## references
https://developer.android.com/guide/components/fundamentals


## Application Fundamentals

Android security features:

- The Android OS is multi-user and each app is its own user
- Unique Linux user ID
- Virtual Machine ( app code runs seperate from other apps)
- different app - different Linux process


Principle of least privilage

- by default an app can only access the information required to do the work and nothing more
- there are ways to set up access to other system services
    - two apps can share a linux ID
    - user has to explicitly grant access to bluetooth, camera etc. 

### App Components

- Activities
    - entry point for the user, a single screen
- Services
    - general purpose entry point to keep app running in background
- Broadcast recievers
    - enables the system to deliver events to the app outside of a regular user flow
- content providers
    - manages a shared set of data that you can store in the file system

### Activating conponents 

- activites, services and broadcast recievers are activated by a message called an intent

intent is and Intent Object

## The manifest File

- AndroidManifest.xml
    - must declare all its components in this file

``` 
In the <application> element, the android:icon attribute points to resources for an icon that identifies the app.

In the <activity> element, the android:name attribute specifies the fully qualified class name of the Activity subclass and the android:label attribute specifies a string to use as the user-visible label for the activity.

You must declare all app components using the following elements:

<activity> elements for activities.
<service> elements for services.
<receiver> elements for broadcast receivers.
<provider> elements for content providers.

```



- 