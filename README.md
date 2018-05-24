# Azure Exercises
*Sample exercises for those learning to code with Azure*

## Sample Exam
Read all the instructions below and all the questions before attempting the exam

###Instructions
* This is a 3 hour, open book exam
    * You may use any non-human resources, online or offline, to help you
* You may **not** communicate (in person or digitally) with any other student or person, except the invigilator 
* Do not write your name anywhere in the source code you submit
    * Use your student number to identify yourself e.g. B01234567
* There are no penalties for asking a question, please clarify any questions you have
* Read the entire question before beginning

###Problem Description
An airline based in Termonfeckin, 'Feckin Flyers', have hired you to develop a Java webapp on Azure. 
Feckin Flyers have daily flights to and from a number of destinations and the international airport in Termonfeckin.
Their app needs to have the following features:
1. A vertical layout with the following:
    1. Show their name and logo at the top of the app 'Feckin Flyers - Termonfeckin's fifth best airline'
        1. The label should use HTML content and the HTML they prefer is: 
        2. <H1>Feckin Flyers</H1> <p/> <h2>Termonfeckin's <strong>fifth</strong> best airline</h2><br>
        3. Note: Don't worry if you don't know HTML, the codes above set the size and positioning of the text
    2. Show a grid with the flights listed. Flights need to be stored in a database table (see below for data)
        1. The left-hand-most column should be a selection column, multiple rows can be selected at once
        2. The first data column should show the time of the flight departure (flights are daily so the date does not have to be shown), and should be labelled "Departs"
        3. The second column should show the departure airport terminal, labelled "From"
        4. The third column should show the destination arrival time, labelled "Arrives"
        5. The fourth column should show the destination airport name, labelled "To"
    3. Under the grid there should be a horizontal layout which has:
        1. A textfield labelled "Full name of passenger"
        2. A ComboBox labelled "Gender", with the values "gentleman" and "lady"
        3. A ComboBox labelled "Status", with the values "infant", "child", "adult"
    4. Under the horizontal layout, a button with "Calculate Cost"
    5. Under the button, an html label which initially shows "Please select the flight(s) above, enter your details and click Calculate Cost" but changes to show the user messages such as:
        1. "<strong>Please select at least one flight!</strong>"
        2. "<strong>Please enter your name!</strong>"
        3. "<strong>Please select gender and status</strong>"
        4. "<h3>The total cost is <strong>€" + cost + "</strong></h3>"
    6.  An mockup image is included below to show how Feckin Flyers would like the UI to look

![The UI Mock-up](/images/ui.png)


###Questions
1. 
2. Create a new Azure app service called
3. Create a SQL database in the same resource group
4. Populate the database with 10 rows of sample data
5. Create a Vaadin app with the following features:
    1. Connects to and loads the data from the database
    2. 