# Azure Exercises
*Sample exercises for those learning to code with Azure*

## Sample Exam
Read all the instructions below and all the questions before attempting the exam

### Instructions
* This is a 3 hour, open book exam
    * You may use any non-human resources, online or offline, to help you
* You may **not** communicate (in person or digitally) with any other student or person, except the invigilator 
* Do not write your name anywhere in the source code you submit
    * Use your student number to identify yourself e.g. B01234567
* There are no penalties for asking a question, please clarify any questions you have
* Read the entire question before beginning

### Problem Description
An airline based in Termonfeckin, 'Feckin Flyers', have hired you to develop a Java webapp on Azure. 
Feckin Flyers have daily flights to a number of destinations from the international airport in Termonfeckin.
They want users of the app to see the flights available, select one or more and get a total cost of the flights. Each flight is €10.50 but some discounts may apply.
They require the user's name to calculate the costs, whether they are a gentleman or lady (ladies get 5 euro off) and whether the flight is for an infant, child or adult. Infants get 75% off, children 50% of the total cost. Feckin Flyers require the user to press the Calculate Costs button each time the user makes a change (such as changing the number of flights).

Test their design: [b01234567-feckinflyers.azurewebsites.net/](https://b01234567-feckinflyers.azurewebsites.net/) 
  
Their app needs to have the following UI:
1. A vertical layout with the following:
    1. Show their name and logo at the top of the app 'Feckin Flyers - Termonfeckin's fifth best airline'.  The label should use HTML content and the HTML they prefer is given below
    2. Show a grid with the flights listed. Flights need to be stored in a database table (see below for data)
        1. The left-hand-most column should be a selection column, multiple rows can be selected at once
        2. The first data column should show the time of the flight departure (flights are daily so the date does not have to be shown), and should be labelled "Departs"
        3. The second column should show the departure airport terminal, labelled "From"
        4. The third column should show the destination arrival time, labelled "Arrives"
        5. The fourth column should show the destination airport name, labelled "To"
    3. Under the grid there should be a horizontal layout which has:
        1. A text field labelled "Full name of passenger"
        2. A ComboBox labelled "Gender", with the values "gentleman" and "lady"
        3. A ComboBox labelled "Status", with the values "infant", "child", "adult"
    4. Under the horizontal layout, a button with "Calculate Cost" as the label
    5. Under the button, an html label which initially shows "Please select the flight(s) above, enter your details and click Calculate Cost" but changes to show the user error messages and the total cost (see below)
    6. A label with your student number (**not your name**)

#### Feckin Flyers have cost calculation rules as follows:
1. You must select at least one flight, but may select as many as you want
2. Each flight costs €10.50
3. A discount of €5 is applied to ladies who are travelling with the airline
4. The total cost (with discount for ladies applied if applicable) is 50% discounted in the case of children and 75% discounted for infants  
    
The total cost label may show one of the following at any time:
```html
Please select the flight(s) above, enter your details and click <strong>Calculate Cost</strong>
<strong>Please select at least one flight!</strong>
<strong>Please enter your name!</strong>"
<strong>Please select gender and status</strong>
<h3>The total cost is <strong>€{123.45}</strong></h3>
```
The HTML code for the logo is supplied by the client:
```html
<H1>Feckin Flyers</H1> <p/> <h2>Termonfeckin's <strong>fifth</strong> best airline</h2><br>
```
*Note: Don't worry if you don't know HTML, the tags above just set the size and positioning of the text, you can copy that directly*

 An mockup image is included below to show how Feckin Flyers would like the UI to look:
![The UI Mock-up](/images/ui.png)

### Requirements
1. Create a new Azure Web app called your student number-feckinflyers e.g. **B01234567-feckinflyers**.azurewebsites.net **(5 marks)**
2. Create a SQL database (and a server) called **B01234567-feckinflyers** in the same resource group **(5 marks)**
3. Populate the database table **flights** with 7 rows of sample data (as above) **(10 marks)**
4. Create a Vaadin app with the following features:
    1. Uses the groupID **ie.ulster.exam**
    2. Connects to and loads the flight data from the Azure database **(5 marks)**
    3. Converts the flight data from a resultset to a List of objects **(5 marks)**
    4. Creates the UI items listed above (marks for adding them and marks for getting each aspect asked in the question implemented) **(25 marks)**
    5. Adds the Calculate Cost functionality so that it correctly prompts the user to fix what they need to **(10 marks)** and then correctly calculates the cost and shows it as directed **(10 marks)**
5. Deploy the app on Azure **(5 marks)**
6. Upload: 
    1. The SQL schema you used to create and populate the database 
    2. pom.xml (put an XML comment with your student number somewhere in the file)
    3. MyUI.java and 
    4. any another java file you created (add a comment to the top of each file with your student number) 
        1. Do not upload any other files automatically created by Vaadin or Maven unless you modified them





