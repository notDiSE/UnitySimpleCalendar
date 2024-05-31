# Unity Simple Calendar
A simple UI calendar for unity

![Calendar](img/Screenshot.png)

# Installation Guide

1. **Download**: Grab the latest package from the [releases page](https://github.com/yourusername/yourrepository/releases).
2. **Import**: Import the package into your project (tested on version 2021.3.14f1)

# How to use
1. **Integrate the Calendar Prefab**:
   - Drag the Calendar prefab into a Canvas within your scene.

2. **Access the Calendar from a Script**:
   - Once the Calendar is part of your scene, you can invoke it from any script using the following example method:
   ```csharp
   async void GetDateFromCalendar()
   {
       DateTime dateTime = await Calendar.GetCalendar();
       Debug.Log($"Selected date and time: {dateTime}");
   }
   ```
   note that the method you call this from has to be async
3.  **Variations**
      - You can also call the Calendar with preselected datetime. For example:
      ```csharp
      async void GetDateFromCalendar()
    {
        DateTime dateTime = await Calendar.GetCalendar(new DateTime(
            0,0,0,0,0,1
            ));
        Debug.Log($"selected dateTime: {dateTime}");
    }
      ```
      - When using preselected DateTime use the seconds to flag if the initial time is set
         - 0 Hours 0 Minutes 0 Seconds means the time has not been preselected
         - 0 Hours 0 Minutes 1 Second means the time has been preselected as 00:00
      - in this example time is also preselected and will be enabled when calendar is shown

# Styling
You can customize the calendar's day appearance with provided script styling options.
Just change the colors in the script inspector.

![Styles](img/Styles.png)



