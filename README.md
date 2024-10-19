# OBJECTIVE 
In this bot we will use Flow chart and Flow Decision activities. The bot talks about how quickly you can decide what to wear today based on the weather. 
## MANUALLY
1) Go to the website and find out the weather today
2) Know the temperature and describe the weather condition
# TECHNICAL REQUIREMENTS

## Arguments panel 
## Workflow.xaml - Invoke Workflow File
1) [Invoke Workflow File](https://docs.uipath.com/ACTIVITIES/other/latest/workflow/invoke-workflow-file)
## UI Automation Activities
1) [Use Application/Browser](https://docs.uipath.com/activities/other/latest/ui-automation%22/n-application-card)
2) [Input Dialog](https://docs.uipath.com/activities/other/latest/workflow/input-dialog)
3) [Log Message](https://docs.uipath.com/activities/other/latest/workflow/log-message)
## Flow Chart Scope
1) [Flow Chart](https://docs.uipath.com/studio/standalone/2023.4/user-guide/flowcharts)
2) [Flow Decision](https://docs.uipath.com/activities/other/latest/workflow/flow-decision)
   
# PROCEDURES
### Main
1) Insert the Input Dialog activity and select the input type (Text Box), save it in a string variable.
2) Use Log Message to Ensure about the name of city that you enter it when the bot had running, active the info option

<img src="https://github.com/user-attachments/assets/21884a76-6723-4cdd-9804-bbd1fe20933a" width="500">


3) Create a new Workflow and use an Invoke Workflow File to invoke it.

### Workflow1
1) Use Browser Chrome: New Tab> Type Into 'editable text', the city name depending on user variable Which was created in main.cityName

2) In step we will use Arguments panel and create one To use the variable that in other workspace. and import it in Invoke Workflow File in the main.

   <img src="https://github.com/user-attachments/assets/c10d28dc-b6ac-4d01-8066-603e0715b320" width="500">
   
   
   .
   <img src="https://github.com/user-attachments/assets/6e0dd2e8-6eb3-43e4-9927-462e4ac97a2d" width="500">
   

3)Using Get Text

    <img src="https://github.com/user-attachments/assets/4c8029ff-f069-47cc-88a9-b4301e27e489" width="500">


 4) Flow Chart Scope> insert a Flow Decision > in the properties panel put the condition.
      
      <img src="https://github.com/user-attachments/assets/23b4e92a-c817-4860-a022-7a6a18f7312f" width="500">


      .
      <img src="https://github.com/user-attachments/assets/7c424413-9f49-486b-99db-dd539b212b79" width="500">
     
      
 5) In True side use assign activity to store "Bring umbrilla" in variable> Message box
 6) In False side insert a new Flow Decision, condtion:Convert.ToInt32 (Tempreture) <20
 7) True Side: "the weather is too cold bring downjacket" , False side: Flow Decision> CInt(Tempreture)> 20
 8) In the end it will be printed using Message Box
     "the weather is" +Tempreture + disctem + "In" + in_CityNameX



# Results
To watch the robot run and the results, [click here](https://drive.google.com/file/d/1xJ0PnmwBDktvYUM8H2IrudmruJvIf8R4/view?usp=drive_link)


# CONCLUSION
   Difference between variable and arguments, variable used just in workflow were created, arguments used to transfer variables.

