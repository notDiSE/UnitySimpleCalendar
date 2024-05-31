# UnitySimpleCalendar
A simple UI calendar for unity

![Calendar](img/Screenshot.png)

# Installation Guide

1. **Download**: Grab the latest package from the [releases page](https://github.com/yourusername/yourrepository/releases).
2. **Import**: Import the package into your project (tested on version 2021.3.14f1)

# How to use
1. Drag the Calendar prefab under a Canvas
2. When the Calendar is in your scene you can call the calendar like this from any script
```csharp
async void GetDateFromCalendar()
{
    DateTime dateTime = await Calendar.GetCalendar();
    Debug.Log($"selected dateTime: {dateTime}");
}
```
4. 



