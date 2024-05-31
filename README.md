# Unity Simple Calendar
A simple UI calendar for unity

![Calendar](img/Screenshot.png)

# Installation Guide

1. **Download**: Grab the latest package from the [releases page](https://github.com/notDiSE/UnitySimpleCalendar/releases).
2. **Import**: Import the package into your project (tested on version 2021.3.14f1)
3. **Input Manager** You need to remove the **return key** from the **Submit action**
   - Project Settins > Input Manager > Submit > *Remove return from the Positive Button*
   - There are 2 Submit actions in the Input Manager, so make sure you do it correctly. (if not, time selection won't work)

# How to use
1. **Integrate the Calendar Prefab**:
   - Drag the Calendar prefab into a Canvas within your scene.
2. **Namespace**
   - in your script make sure you use the AP namespace
   ```csharp
   using AP;
   ```

4. **Access the Calendar from a Script**:
   - Once the Calendar is part of your scene, you can invoke it from any script using the following example method:
   ```csharp
   async void GetDateFromCalendar()
   {
       DateTime dateTime = await Calendar.GetCalendar();
       Debug.Log($"Selected date and time: {dateTime}");
   }
   ```
   note that the method you call this from has to be async
5.  **Variations**
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

# Time/No Time
The calendar gives the user the option to select time or not.
When the calendar returns dateTime it uses the seconds as a flag to if the time has been selectd or not 
         - 0 Hours 0 Minutes 0 Seconds means the time has not been selected
         - 0 Hours 0 Minutes 1 Second means the time has been selected as 00:00
         
# Testing the Calendar
You can test the calendar using the **Test Open Calendar** button located at the bottom of the Calendar script.t

# Styling
You can customize the calendar's day appearance with provided script styling options.
Just change the colors in the script inspector.

![Styles](img/Styles.png)

# Changing the months
You can change the names of the months in the inspector of the Calendar script.




