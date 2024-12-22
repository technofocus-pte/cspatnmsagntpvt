<img src="./media/image1.png"
style="width:6.19167in;height:2.39167in" />

**Level-up CSP Technical Training – Autonomous Agent Facilitator
Guide  **

Automating Employee Onboarding with the Contoso Onboarding Agent

Lab Guide for Onboarding Employee Scenario

| Description | Contoso Solutions aims to automate its employee onboarding process with the Contoso Onboarding Agent. This solution streamlines the process by automating tasks such as collecting new hire information, creating employee accounts, and scheduling orientation. New employees submit an onboarding form, and the agent extracts the data, creates accounts, and sends an automated email with essential details. HR Manager Miriam benefits by reducing manual work, allowing her to focus on strategic tasks. New employee Jane enjoys a smooth, efficient onboarding experience with all necessary information delivered automatically. |
|----|----|
| Prerequisites | To begin the lab, you will need admin tenant or work/school credentials for accessing Microsoft services, a Copilot Studio Viral Trial License and Power Apps Trial License for creating and testing automation, an active email ID for communication, the company policy document for compliance, and an employee onboarding Excel sheet to collect and manage employee data. |
| Duration | 60 mins |
| Version | 1.0 |
| Publication date  | December 2024 |

This document is provided “as-is”. Information and views expressed in
this document, including URL and other Internet Web site references, may
change without notice. You bear the risk of using it. 

This document does not provide you with any legal rights to any
intellectual property in any Microsoft product. You may copy and use
this document for your internal reference purposes. 

 

© 2024 Microsoft. All rights reserved.  

### Objective

To automate the employee onboarding process at Contoso Solutions by
building the **Contoso Onboarding Agent**. This agent will collect
information from new hires, create necessary accounts, schedule
orientation, and send all relevant details to the new employee,
significantly reducing manual effort in the onboarding process.

### Solution Focus Area:

At Contoso Solutions, the HR department faces a manual and
time-consuming onboarding process. New employees must fill out an
onboarding form, and HR personnel manually enter this information,
create employee IDs, generate email addresses, Assign Laptop, Assign
Parking pass and schedule orientation sessions.

To address this, Contoso Solutions seeks to automate the entire
onboarding process. The **Contoso Onboarding Agent** will handle data
extraction, account creation, orientation scheduling, and communication
with new hires, improving both efficiency and accuracy.

### Solution

The **Contoso Onboarding Agent** will automate the key tasks involved in
the employee onboarding process:

- **Employee Form Submission:** New employees fill out an onboarding
  form that includes essential details such as personal information, job
  role, and department.

- **Data Extraction and Storage:** The agent automatically extracts the
  employee details from the form and saves the information into
  **Dataverse**, centralizing the data for easy management.

- **Account Creation:** Using the extracted information, the agent
  creates a unique **Employee ID**. Generates an **employee email
  address** based on company conventions.

- **Automated Email Communication:** The agent sends a confirmation
  email to the new employee containing, **Employee ID**, **Employee
  email address**, **Orientation session details**, including date,
  time, and location, Parking Pass and Assigned Laptop details.

### Persona

**Miriam Graham – HR Manager**

Miriam, the HR Manager at Contoso Solutions, has long struggled with the
manual onboarding process, which involves reviewing forms, creating
accounts, and scheduling orientations. With the implementation of the
**Contoso Onboarding Agent**, these tasks are automated. Now, Miriam can
focus on more strategic HR duties while the agent handles employee data
collection, account creation, and orientation scheduling, making the
onboarding process quicker and more efficient.

**Jane Miller – New Employee Python Developer**

Jane, a new Python Developer at Contoso, was worried about the usual
slow and paperwork-heavy onboarding process. However, after submitting
her onboarding form, she receives an email from the **Contoso Onboarding
Agent** with her **Employee ID, email address, assigned laptop details,
Parking Pass** and **orientation details**. This seamless process allows
Jane to start her role quickly and confidently, with all necessary
information delivered automatically.

### Pre-requisite

1.  Admin tenant credential or Work / School Credentials

2.  Copilot Studio Viral Trial License

3.  Power Apps Trial License

4.  OneDrive

5.  Email ID

6.  Company Policy Document

7.  Employee Onboarding Excel Sheet

###  

## Exercise 1: Creating the Contoso Onboarding Agent

In this exercise, participants will create and configure an autonomous
agent, the "Contoso Onboarding Agent," using Microsoft Copilot Studio.
This agent streamlines the employee onboarding process by automating
data collection, ID generation, email creation, and notifications.
Through this hands-on experience, participants will learn to integrate
generative AI, Dataverse, and Power Automate for seamless operation.

### Task 1: Logging into Microsoft Copilot Studio

1.  Navigate to copilot studio website
    <https://www.microsoft.com/en-us/microsoft-copilot/microsoft-copilot-studio>
    and click on the **Try free.**

<img src="./media/image2.png"
style="width:6.26806in;height:2.87222in" />

2.  Enter admin tenant ID / work or school ID in the respected field and
    click on the **Next** button.

**Note:** For this lab we are using admin tenant credentials,
participant can use their work or school id to start free trial.

<img src="./media/image3.png"
style="width:6.26806in;height:2.79583in" />

3.  Enter **Country or Region** and **Business phone number** in the
    respected fields. Select the check box and click on **Get started**
    button.

<img src="./media/image4.png"
style="width:6.26806in;height:3.54931in" />

4.  In the confirmation section again click on the **Get Started**
    button.

<img src="./media/image5.png"
style="width:6.26806in;height:2.52778in" />

### Task 2: Creating and Configuring Contoso Onboarding Agent 

1.  In copilot studio home section from top select the environment
    development environment**.** In our case its **Dev One** participant
    chooses their environment.

<img src="./media/image6.png"
style="width:6.26806in;height:3.03264in" />

2.  On the welcome copilot studio tab, click on the **Skip** to move
    forward.

<img src="./media/image7.png"
style="width:5.41065in;height:4.86004in" />

3.  From the left navigation bar select **Create** and then select **New
    agent** to start creating new agent.

<img src="./media/image8.png"
style="width:6.26806in;height:2.83542in" />

4.  From the top right corner click on **Skip to configure** button.

<img src="./media/image9.png"
style="width:6.26806in;height:2.80903in" />

5.  Enter **Name, Description and Instruction** of the agent as given
    below and click on **Create** button.

> **Name:** Contoso Onboarding Agent
>
> **Description:** The Contoso Onboarding Autonomous Agent automates
> employee onboarding by saving form data to Dataverse, generating an
> employee ID and email, and sending a welcome email—all triggered
> seamlessly via Power Automate.
>
> **Instruction:** Create a new bot, configure its name and language,
> and connect it to Dataverse or other data sources. Define topics and
> triggers for the bot, use AI capabilities to refine responses, and
> integrate Power Automate for advanced actions like ID generation or
> email notifications. Test and publish the bot to make it live.
>
> <img src="./media/image10.png"
> style="width:6.26806in;height:2.82222in" />

6.  On the overview page of Contoso Onboarding Agent, **Enable** the
    orchestrator for the agent.

<img src="./media/image11.png"
style="width:6.26806in;height:3.09028in" />

7.  On the overview page of the agent, **Disable** the “**Allow the AI
    to use its own general knowledge**” option.

<img src="./media/image12.png"
style="width:6.26806in;height:3.38472in" />

8.  From the top right corner of the agent, click on the **Settings**
    button.

<img src="./media/image13.png"
style="width:6.26806in;height:2.76875in" />

9.  Then go to Generative AI section, select the Generative AI
    (Preview), set content moderation as **Medium** and click on
    **Save** to save the setting.

<img src="./media/image14.png"
style="width:6.26806in;height:2.62083in" />

### Conclusion

By completing this exercise, participants will learn:

- Learned to log in and set up Microsoft Copilot Studio.

- Created and configured the "Contoso Onboarding Agent."

- Integrated Dataverse for data storage and Power Automate for
  workflows.

- Enabled generative AI to enhance agent capabilities.

- Gained skills in designing intelligent bots for process automation.

## Exercise 2: Getting Started with Power Apps

In this exercise, participants will explore the basics of Power Apps by
logging into the platform and setting up a Dataverse table. This
hands-on activity helps participants understand the foundational steps
for using Power Apps to manage and structure data efficiently.

### Task 1: Logging into Power Apps

1.  Navigate to power apps website
    <https://www.microsoft.com/en-us/power-platform/products/power-apps>
    and click on the **Try for Fre**e **button.**

> <img src="./media/image15.png"
> style="width:6.26042in;height:2.82292in" />

2.  Enter admin tenant id / work or school id, check the box and click
    on **Start free,** for this tab we are using admin tenant id.

<img src="./media/image16.png"
style="width:6.26806in;height:3.94236in" />

3.  Enter Country/ Region, Phone number, select box check box and click
    on the **Get started**.

> <img src="./media/image17.png"
> style="width:6.26042in;height:3.04167in" />

4.  Confirm the account details and then click on the **Get started**.

> <img src="./media/image18.png"
> style="width:6.26042in;height:3.07292in" />

5.  On the Stay signed in tab select **Yes**.

<img src="./media/image19.png"
style="width:6.26806in;height:3.11389in" />

### Task 2: Setting Up a Dataverse Table

1.  On the power apps home page, from top select the development
    environment. In our case its **Dev One**, participant can choose
    their own environment.

<img src="./media/image20.png"
style="width:6.26806in;height:2.86111in" />

2.  From the left navigation bar select **Tables.** In the tables
    section top bar click on the **+ New table** and then select
    **Create new tables**.

<img src="./media/image21.png"
style="width:6.26806in;height:2.83194in" />

3.  Select **Import an Excel file or CSV** option to create a new table.

<img src="./media/image22.png"
style="width:6.26806in;height:2.40903in" />

4.  Click on the select form device option and select **Employee
    Onboarding** excel file from **Lab Files** folder.

<img src="./media/image23.png"
style="width:6.26806in;height:2.92014in" />

5.  Select the table and click on **View data** to see the table.

**Note:** In my case, the table is named *Employee Record*. The name may
vary with each execution. Please save the table name for future
reference.

<img src="./media/image24.png"
style="width:6.26806in;height:2.48403in" />

6.  Click on the first row of the table and click on the **Delete
    rows**.

<img src="./media/image25.png"
style="width:6.26806in;height:1.23819in" />

7.  Scroll right and click on the down arrow of **Onboarding Session
    Date and Time**, select **Text 🡪 Single line of text** as data type
    and then select **Update**. Repeat the same process with **Training
    Date and Time, Date of Birth and Start Date** columns.

<img src="./media/image26.png"
style="width:6.26806in;height:2.43542in" />

<img src="./media/image27.png"
style="width:6.26806in;height:2.23194in" />

<img src="./media/image28.png"
style="width:6.26806in;height:2.48611in" />

<img src="./media/image29.png"
style="width:6.26806in;height:3.01528in" />

8.  From the top right corner, click on the **Save and exit** to save
    the table.

<img src="./media/image30.png"
style="width:6.26806in;height:1.43889in" />

### Conclusion

By completing this exercise, participants will learn:

- Learned to log in and navigate the Power Apps interface.

- Created a Dataverse table by importing and configuring data.

- Gained practical experience in managing and preparing data for Power
  Apps.

- Acquired foundational skills to build data-driven applications using
  Power Apps.

## Exercise 3: Enhancing the Contoso Onboarding Agent

In this exercise, participants will enhance the functionality of the
Contoso Onboarding Agent by adding knowledge sources, customizing the
conversation start topic, and updating fallback responses. These steps
improve the agent's ability to provide relevant information and handle
user interactions effectively.

### Task 1: Adding Knowledge Sources

1.  Navigate back to Contoso onboarding agent overview page, scroll down
    and click on the **+ Add knowledge** button.

<img src="./media/image31.png"
style="width:6.26806in;height:3.14653in" />

2.  Select **Click to browse** button and select **Company policy**
    document from the Lab files folder.

<img src="./media/image32.png"
style="width:6.26806in;height:4.11944in" />

<img src="./media/image33.png"
style="width:6.22554in;height:3.65032in" />

3.  After selection of the file click on the **Add** button to add the
    file into the knowledge base.

<img src="./media/image34.png"
style="width:6.26806in;height:4.12778in" />

4.  Navigate to agent overview page, scroll down and click on the **+
    Add knowledge** button.

<img src="./media/image35.png"
style="width:6.26806in;height:2.77917in" />

5.  Select the **Dataverse** table as knowledge source.

<img src="./media/image36.png"
style="width:6.26806in;height:3.11389in" />

6.  Then search for **Employee Record** and select the table. After
    selecting table click on the **Next, Next and the Add button.**

<img src="./media/image37.png"
style="width:6.26806in;height:4.08194in" />

<img src="./media/image38.png"
style="width:6.26806in;height:4.04722in" />

<img src="./media/image39.png"
style="width:6.26806in;height:4.08819in" />

### Task 2: Customize the Conversation Start Topic

1.  From the top bar option click on **Topics** and then click and open
    **Conversation Start** topic.

<img src="./media/image40.png"
style="width:5.77125in;height:3.54101in" />

2.  Scroll down and go to message node. Replace the message after
    “Hello. I’m Bot Name, a virtual assistant” as given below:

Hello. I’m Bot Name, a virtual assistant. How can I help you?

<img src="./media/image41.png"
style="width:6.26806in;height:3.70347in" />

3.  From top click on the **Save** to save the topic.

<img src="./media/image42.png"
style="width:6.26806in;height:3.71875in" />

###  Task 3: Update the Fallback Topic 

1.  From the top bar option click on **Topics** and then click and open
    **Fallback** topic.

<img src="./media/image43.png"
style="width:6.26806in;height:3.80417in" />

2.  Scroll down and go to message node. Update the message as given
    below:

I’m sorry. This information is not available in my system.

<img src="./media/image44.png"
style="width:6.26806in;height:3.38681in" />

3.  From top right side click on the **Save** button to save the topic.

<img src="./media/image45.png"
style="width:6.26806in;height:3.76181in" />

### Conclusion

By completing this exercise, participants will learn:

- Learned to enhance agent functionality by adding knowledge sources.

- Customized conversation topics to improve user interaction.

- Updated fallback responses for better handling of unsupported queries.

- Gained insights into refining virtual assistant capabilities for an
  improved user experience.

## Exercise 4: Testing the Contoso Onboarding Agent

In this exercise, participants will test the Contoso Onboarding Agent to
ensure its functionality and verify its responses to user prompts. This
process is critical to validating the agent's knowledge sources and
conversational accuracy.

1.  From top right corner click on the **Test** button. Then in test
    section click on **Map** turn it **on** and then click **Refresh**.

<img src="./media/image46.png"
style="width:6.26806in;height:2.7625in" />

2.  Enter the prompt “**Give me the information about the employee
    benefits**.**”.**

<img src="./media/image47.png"
style="width:6.26806in;height:2.75208in" />

3.  Again, give the prompt **“Give me the company policy details”.**

<img src="./media/image48.png"
style="width:6.26806in;height:2.75417in" />

4.  It will return all the company policy details.

<img src="./media/image49.png"
style="width:6.26806in;height:2.73819in" />

### Conclusion

By completing this exercise, participants will learn:

- Learned to test the agent using the built-in test feature.

- Verified the agent’s ability to retrieve employee benefits and company
  policy information.

- Ensured the agent operates correctly and provides accurate responses.

- Gained experience in validating and fine-tuning virtual assistant
  performance.

## Exercise 5: Creating and Testing the Employee Onboarding Flow

In this exercise, participants will automate an employee onboarding
process using Microsoft Power Automate and Copilot integration. By
creating a flow that dynamically collects employee details, generates an
onboarding email, and creates a parking pass, participants will learn
how to integrate Dataverse, OneDrive, and Office 365 seamlessly. This
exercise demonstrates how automation can streamline HR processes,
ensuring accuracy and efficiency.

### Task 1: Create the Employee Onboarding Flow

1.  Go to overview page of the agent, scroll down and click on the **+
    Add action**.

<img src="./media/image50.png"
style="width:6.26806in;height:3.2625in" />

2.  In choose an action window, scroll down and click on **Create a new
    flow**, power automate flow window will open.

<img src="./media/image51.png"
style="width:6.26806in;height:4.17986in" />

3.  In Power automate flow, click on **Run a flow from copilot** and
    then select **Add an Input**.

<img src="./media/image52.png"
style="width:6.26806in;height:3.00347in" />

4.  Select **Text** as data type of input and rename the input as **Full
    Name**.

<img src="./media/image53.png"
style="width:6.26806in;height:3.76597in" />

<img src="./media/image54.png"
style="width:5.7255in;height:2.35854in" />

5.  With same procedure create more input as per given below details.

| **Input Name** | **Data Type** |
|----------------|---------------|
| Job Title      | Text          |
| Start Date     | Text          |
| Date of Birth  | Text          |
| Contact Number | Text          |
| Personal Email | Text          |
| Address        | Text          |
| Laptop         | Text          |
| Vehicle Number | Text          |

<img src="./media/image55.png"
style="width:6.26806in;height:6.08194in" />

6.  Below Run a flow from copilot, click on **(+)** sign and select
    **Add an action**.

<img src="./media/image56.png"
style="width:6.26806in;height:3.26667in" />

7.  In the action search bar, search for **Add a new row** and select
    **Add a new row** from **Dataverse** section.

<img src="./media/image57.png"
style="width:5.64216in;height:4.1837in" />

> Note: Sometimes Dataverse connection is not created automatically, so
> participant need to **sign** in with their credential, authentication
> should be **OAuth.**
>
> <img src="./media/image58.png"
> style="width:6.26042in;height:3.07292in" />

8.  Search and select **Employee Record** table, in the table section.

<img src="./media/image59.png"
style="width:6.26806in;height:2.57431in" />

9.  Below table name select **Show all**, then click on the particular
    field and add input with the help of dynamic content button (Thunder
    bolt) as per the below given field.

| **Section**    | **Input Variable**                        |
|----------------|-------------------------------------------|
| Address        | Address (Dynamic Content Variable)        |
| Contact Number | Contact Number (Dynamic Content Variable) |
| Date of birth  | Date of birth (Dynamic Content Variable)  |
| Full Name      | Full Name (Dynamic Content Variable)      |
| Job Title      | Job Title (Dynamic Content Variable)      |
| Laptop         | Laptop (Dynamic Content Variable)         |
| Personal Email | Personal Email (Dynamic Content Variable) |
| Start Date     | Start Date (Dynamic Content Variable)     |
| Vehicle Number | Vehicle Number (Dynamic Content Variable) |

<img src="./media/image60.png"
style="width:5.50048in;height:0.92508in" />**  
**

<img src="./media/image61.png"
style="width:5.0421in;height:4.69207in" />

10. For some other fields, click on the particular field and add input
    with the help of **Expression option (Fx)** 🡪 **Create an expression
    with copilot** as per the below given field.

<img src="./media/image62.png"
style="width:5.54215in;height:0.8084in" />

<img src="./media/image63.png"
style="width:6.26806in;height:2.95486in" />

1.  To generate the **Employee email**, navigate to expression section
    of the field, select the **Create an expression with copilot**
    option and enter the prompt “create an employee email with the help
    of Full name (Remove all the space from full name) and
    @contoso.com”. Click on the **Create expression 🡪** **Ok** and then
    **Add** to add the expression.

> <img src="./media/image64.png"
> style="width:3.85033in;height:2.39187in" />
>
> <img src="./media/image65.png"
> style="width:4.09202in;height:5.55881in" />
>
> <img src="./media/image66.png"
> style="width:4.35038in;height:5.7755in" />

2.  To generate the **Employee ID**, navigate to expression section of
    the field, select the **Create an expression with copilot** option
    and enter the prompt “create employee id with CONTOSO and Last 4
    digit of mobile number”. Click on the **Create expression** 🡪 **Ok**
    and then **Add** to add the expression.

> <img src="./media/image64.png"
> style="width:3.85033in;height:2.39187in" />
>
> <img src="./media/image67.png"
> style="width:4.2087in;height:5.50881in" />
>
> <img src="./media/image68.png"
> style="width:4.12536in;height:5.79217in" />

3.  To generate the **Onboarding Session Date and Time**, navigate to
    expression section of the field, select the **Create an expression
    with copilot** option and enter the prompt “Concat Start date,
    space, 12 PM”. Click on the **Create expression** 🡪 **Ok** and then
    **Add** to add the expression.

> <img src="./media/image64.png"
> style="width:3.85033in;height:2.39187in" />
>
> <img src="./media/image69.png"
> style="width:3.65865in;height:5.0171in" />
>
> <img src="./media/image70.png"
> style="width:3.94201in;height:5.21712in" />

4.  To generate the **Training Date and Time**, navigate to expression
    section of the field, select the **Create an expression with
    copilot** option and enter the prompt “Concat Start date, space, 04
    PM”. Click on the **Create expression** 🡪 **Ok** and then **Add** to
    add the expression.

> <img src="./media/image64.png"
> style="width:3.85033in;height:2.39187in" />
>
> <img src="./media/image71.png"
> style="width:4.10869in;height:5.55881in" />
>
> <img src="./media/image72.png"
> style="width:4.21703in;height:5.71716in" />

11. Below Add a new row trigger, click on the **+** icon and select
    **Add an action.**

<img src="./media/image73.png"
style="width:6.26806in;height:4.03194in" />

12. Search for Create file and select **Create file** from OneDrive
    Business.

<img src="./media/image74.png"
style="width:5.58382in;height:4.25037in" />

13. Click on the **Sign in** and sign in with the help of tenant
    credentials.

<img src="./media/image75.png"
style="width:5.09211in;height:2.80858in" />

14. Enter the below given details in the respected section of the create
    file action.

<table>
<colgroup>
<col style="width: 22%" />
<col style="width: 77%" />
</colgroup>
<thead>
<tr>
<th>Folder Path</th>
<th>Click on the folder icon and select Root</th>
</tr>
</thead>
<tbody>
<tr>
<td>File Name</td>
<td>Parking Pass Full Name (Choose the dynamic Variable Full Name with
the help of thunder bolt option)</td>
</tr>
<tr>
<td>Content</td>
<td><p>Contoso Parking Pass<br />
<br />
Name: (Choose the dynamic Variable Full Name with the help of thunder
bolt option)</p>
<p>Vehicle Number: (Choose the dynamic Variable Vehicle Number with the
help of thunder bolt option)</p></td>
</tr>
</tbody>
</table>

<img src="./media/image76.png"
style="width:5.19212in;height:3.97534in" />

15. Click on the **+** icon below create file and search for **Create
    share link by path** and select **Create share link by path** from
    **OneDrive for Business**.

<img src="./media/image77.png"
style="width:6.26806in;height:5.00972in" />

16. In the Create share link by path action, enter the following detail:

| File Path | Select the Path dynamic variable with the help of thunder bolt option under create file dynamic variable |
|----|----|
| Link Type | With drop down select View |

<img src="./media/image78.png"
style="width:6.26806in;height:2.86042in" />

17. Click on the + icon below **share link** and search for **send an
    email action** and select **send an email (v2)** from office 365
    outlook.

<img src="./media/image79.png"
style="width:6.26806in;height:4.20903in" />

18. On send an email action click on the **Switch to Advanced mode**
    option.

<img src="./media/image80.png"
style="width:5.83384in;height:2.54189in" />

19. In Send an email option enters the below given details in the
    respected sections. There is some information are missing in the
    given below body please insert information in front of the text as
    given below:

<table>
<colgroup>
<col style="width: 18%" />
<col style="width: 81%" />
</colgroup>
<thead>
<tr>
<th>To</th>
<th>Select Personal Email from Dynamic content (thunder bolt)
option</th>
</tr>
</thead>
<tbody>
<tr>
<td>Subject</td>
<td>Welcome to Contoso! Your Onboarding Information</td>
</tr>
<tr>
<td>Body</td>
<td><p>Dear, (Full Name)</p>
<p>Welcome to Contoso! We are delighted to have you as part of our team
and are excited about the contributions you will bring.</p>
<p>Below are some essential details and resources to help you get
started:</p>
<p>Your Employee Details</p>
<p>Employee ID: (Employee ID)</p>
<p>Employee Email: (Employee Email)</p>
<p>Parking Pass: (Select Create file path link from dynamic option)</p>
<p>Laptop Assignment: (Laptop)</p>
<p>We have scheduled an onboarding session to help you transition
smoothly into your role at Contoso:</p>
<p>Date: and Time: (Onboarding session Date and Time)</p>
<p>30 days training employee program will start from (Training Date and
Time)</p>
<p>If you have any questions or need assistance, feel free to reach out.
We are here to support you every step of the way.</p>
<p>Once again, welcome to the Contoso family!</p>
<p>Best Regards,</p>
<p>Team HR</p></td>
</tr>
</tbody>
</table>

**Full Name:** Select the dynamic variable **Full Name** with the help
of thunder bolt option.

**Laptop:** Select the dynamic variable **Laptop** with the help of
thunder bolt option.

**Parking Pass:** Select the dynamic variable **Path** with the help of
thunder bolt option from create file section.

**Employee ID:** Select expression option (fx) and follow the step to
create the expression same as we create for Add a new row (Dataverse)
action.

**Employee Email:** Select expression option (fx) and follow the step to
create the expression same as we create for Add a new row (Dataverse)
action.

**Onboarding Session Date and Time:** Select expression option (fx) and
follow the step to create the expression same as we create for Add a new
row (Dataverse) action.

**Training Date and Time:** Select expression option (fx) and follow the
step to create the expression same as we create for Add a new row
(Dataverse) action.

<img src="./media/image81.png"
style="width:6.26806in;height:4.13472in" />

20. From the top left side of the window rename the flow as **Employee
    Onboarding.**

<img src="./media/image82.png"
style="width:6.26806in;height:1.71181in" />

21. From Top bar click on **Save draft** and then select **Publish**.

<img src="./media/image83.png"
style="width:6.26806in;height:1.74375in" />

### Task 2: Configure and Finalize the Flow in Copilot

1.  Go back to copilot window and click on the **Refresh** button.

<img src="./media/image84.png"
style="width:6.26806in;height:3.83472in" />

2.  From choose an action window, select **Employee Onboarding** flow.
    After that click on the **Next** button.

<img src="./media/image85.png"
style="width:6.26806in;height:4.13958in" />

<img src="./media/image86.png"
style="width:6.26806in;height:4.13611in" />

3.  From top right corner click on the **Edit Input** option.

<img src="./media/image87.png"
style="width:6.26806in;height:3.43681in" />

4.  Add the description of each input as given below:

| Full Name      | Enter the Full Name of the employee      |
|----------------|------------------------------------------|
| Contact Number | Enter the Contact Number of the employee |
| Address        | Enter the Address of the employee        |
| Laptop         | Enter the Laptop of the employee         |
| Start Date     | Enter the Start Date of the employee     |
| Date of Birth  | Enter the Date of Birth of the employee  |
| Job Title      | Enter the Job Title of the employee      |
| Personal Email | Enter the Personal Email of the employee |
| Vehicle Number | Enter the Vehicle Number of the employee |

<img src="./media/image88.png"
style="width:4.36086in;height:2.89355in" />

5.  Then again click on the **Next** button and the select **Finish**.

<img src="./media/image89.png"
style="width:6.26806in;height:4.21736in" />

<img src="./media/image90.png"
style="width:6.26806in;height:4.18681in" />

### Conclusion

By completing this exercise, participants will learn:

- Successfully created an Employee Onboarding flow integrating Copilot
  and Power Automate.

- Automated key onboarding tasks such as generating employee records and
  sending emails.

- Configured dynamic inputs, file creation, and email notifications for
  a seamless process.

- Validated the flow functionality by linking it with Copilot actions.

## Exercise 6: Creating an Employee Onboarding Form in Microsoft Forms

In this exercise, participants will learn how to create an employee
onboarding form using Microsoft Forms. They will log in, create a new
form, and add relevant fields such as Full Name, Job Title, Contact
Information, and more, while configuring the form to collect responses.

1.  Navigate to Microsoft forms website
    <https://www.microsoft.com/en-gb/microsoft-365/online-surveys-polls-quizzes>
    and click on the **Sign in** button.

<img src="./media/image91.png"
style="width:6.26806in;height:2.89722in" />

2.  Enter the admin tenant id / work or school id on the field and click
    on the **Next** button.

<img src="./media/image92.png"
style="width:6.26806in;height:3.38611in" />

3.  Enter the password in the respected field and then click on the
    **Sign in** button.

<img src="./media/image93.png"
style="width:6.26806in;height:2.95278in" />

4.  Select **Yes** to stay signed in Microsoft forms.

<img src="./media/image94.png"
style="width:6.26806in;height:2.78819in" />

5.  From top left click on the **New Form** to start creating new form.

<img src="./media/image95.png"
style="width:6.26806in;height:3.14861in" />

6.  Add the heading "**Employee Onboarding Form**" to the form and
    create the following fields with their respective types. Turn on
    **Required** for all fields.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 49%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;">Field Name</th>
<th style="text-align: center;">Type</th>
</tr>
</thead>
<tbody>
<tr>
<td>Full Name</td>
<td>Text</td>
</tr>
<tr>
<td>Job Title</td>
<td>Text</td>
</tr>
<tr>
<td>Contact Number</td>
<td>Text</td>
</tr>
<tr>
<td>Personal Email</td>
<td>Text</td>
</tr>
<tr>
<td>Address</td>
<td>Text</td>
</tr>
<tr>
<td>Date of Birth</td>
<td>Date</td>
</tr>
<tr>
<td>Start Date</td>
<td>Date</td>
</tr>
<tr>
<td>Laptop</td>
<td><p>Choice</p>
<ol type="1">
<li><p>Surface Go 3</p></li>
<li><p>Surface Pro 2</p></li>
<li><p>Surface Studio 2</p></li>
</ol></td>
</tr>
<tr>
<td>Vehicle Number</td>
<td>Text</td>
</tr>
</tbody>
</table>

<img src="./media/image96.png"
style="width:6.26806in;height:2.69861in" />

7.  From top click on the **Collect responses** button and **Copy** the
    URL.

<img src="./media/image97.png"
style="width:6.26806in;height:2.40486in" />

<img src="./media/image98.png"
style="width:6.26806in;height:2.42222in" />

8.  Open new window tab and paste the URL and open the form.

<img src="./media/image99.png"
style="width:6.26806in;height:3.32639in" />

### Conclusion

By completing this exercise, participants will learn:

- Successfully created an employee onboarding form in Microsoft Forms
  with essential fields like Full Name, Job Title, Contact Information,
  and more.

- Configured the form to collect responses, making it easy to gather
  data from employees.

- The form is now ready for sharing and collecting responses via a URL
  link.

## Exercise 7: Creating and Configuring a Trigger for Employee Onboarding Form Responses

In this exercise, participants will create a trigger to initiate an
action when a new response is submitted through the Employee Onboarding
Form. They will configure the trigger to collect form data and run the
Employee Onboarding flow by using dynamic content.

1.  Navigate to overview page of the agent, scroll down and click on
    the + Add trigger button.

<img src="./media/image100.png"
style="width:6.26806in;height:2.65764in" />

2.  From top right corner search and then select **When a new response
    is submitted trigger.**

<img src="./media/image101.png"
style="width:6.26806in;height:4.4375in" />

3.  After successfully creation of connection, and the green tick appear
    on the trigger click on the **Next**.

<img src="./media/image102.png"
style="width:5.43067in;height:3.8904in" />

4.  Select Employee Onboarding Form as Form ID and then click on the
    **Create Trigger.** After creating trigger click on the **Close**.

<img src="./media/image103.png"
style="width:5.13106in;height:3.67235in" />

<img src="./media/image104.png"
style="width:6.26806in;height:4.41597in" />

5.  Navigate to overview page of agent, scroll down on trigger section
    click on the three dot and then select Edit in power automate
    button.

<img src="./media/image105.png"
style="width:6.26806in;height:3.30694in" />

6.  On the power automate flow, right click on the When a new response
    is submitted trigger click on **Delete** and then select **Ok**.

<img src="./media/image106.png"
style="width:6.26806in;height:3.42917in" />

<img src="./media/image107.png"
style="width:6.26806in;height:1.94792in" />

7.  Select Add a trigger option and search and select **When a new
    response is submitted action.**

<img src="./media/image108.png"
style="width:6.26806in;height:2.36806in" />

8.  In the trigger, select **Employee Onboarding Form** as Form ID.

<img src="./media/image109.png"
style="width:6.26806in;height:2.27222in" />

9.  Below trigger, click on the **+** icon, then search and select **Get
    Response Details** action.

<img src="./media/image110.png"
style="width:6.26806in;height:2.62708in" />

10. In Get response detail action select **Employee Onboarding Form** as
    form ID and **Response ID** as dynamic input variable.

<img src="./media/image111.png"
style="width:6.26806in;height:3.44167in" />

11. Select Send a prompt action, In the Body/Message of send a prompt
    action, enter the below given content.

Run Employee Onboarding flow and use content from Full Name, Job Title,
Contact Number, Personal Email, Address, Date of Birth, Start Date,
Laptop, Vehicle Number.

Note: Replace “Full Name, Job Title, Contact Number, Personal Email,
Address, Date of Birth, Start Date, Laptop, Vehicle Number.” With
dynamic content variable.

<img src="./media/image112.png"
style="width:5.47612in;height:2.08282in" />

12. From top click on the **Save draft** and then select **Publish**.

<img src="./media/image113.png"
style="width:5.33266in;height:1.79193in" />

### Conclusion

By completing this exercise, participants will learn:

- Successfully created a trigger to capture new responses from the
  Employee Onboarding Form.

- Configured the flow to use dynamic content variables such as Full
  Name, Job Title, and more to initiate actions when a response is
  submitted.

- The flow was saved and published, ready to run automatically upon form
  submission.

## Exercise 8: Testing the Employee Onboarding Flow Trigger

In this exercise, participants will test the trigger for the Employee
Onboarding flow. They will manually submit the form to simulate the
trigger and ensure the connection and flow actions are properly
executed.

1.  From the Trigger flow, click on the test button.

<img src="./media/image114.png"
style="width:6.26806in;height:1.23125in" />

2.  Select Manually as option and then again click on the **Test**
    button.

<img src="./media/image115.png"
style="width:2.35796in;height:3.44323in" />

3.  Open the form window where we paste and open the form URL enter all
    the detail and submit the form.

<img src="./media/image116.png"
style="width:6.26806in;height:3.22222in" />

<img src="./media/image117.png"
style="width:6.26806in;height:2.88194in" />

4.  After trigger test is complete, navigate back to the copilot window.

<img src="./media/image118.png"
style="width:6.26806in;height:2.59236in" />

5.  Navigate to overview page of the agent, scroll down and click on the
    **Test** button on the trigger section and the select **Start
    Testing**.

<img src="./media/image119.png"
style="width:6.26806in;height:2.44861in" />

<img src="./media/image120.png"
style="width:6.26721in;height:3.35862in" />

6.  On the test section, connection permission is reflected. Click on
    the **Connect**.

<img src="./media/image121.png"
style="width:4.00868in;height:2.31687in" />

7.  On the Manage Connection window click on the **Connect** and the
    **Submit** the connection. After successful creation of connection,
    it shows **Connected**.

<img src="./media/image122.png"
style="width:6.26806in;height:2.00833in" />

<img src="./media/image123.png"
style="width:6.26806in;height:4.26806in" />

<img src="./media/image124.png"
style="width:6.26806in;height:1.93125in" />

8.  Navigate back to the agent overview page, scroll down and click on
    the **Test** button, after selecting test button click on **Start
    Testing**.

<img src="./media/image125.png"
style="width:6.26806in;height:2.16111in" />

<img src="./media/image126.png"
style="width:6.06719in;height:2.79191in" />

9.  The test case is executed, all the information is saved in the
    Dataverse table, and onboarding mail is sent to the new employee.

<img src="./media/image127.png"
style="width:6.26806in;height:2.28194in" />

<img src="./media/image128.png"
style="width:6.26806in;height:3.68056in" />

10. Check the information of the employee in the **Dataverse** table.

<img src="./media/image129.png"
style="width:6.26806in;height:1.00694in" />

11. Enter the Prompt “**I want to know about the Jane Miller Onboarding
    date and time.**” in the copilot test window. It returns the
    information related to prompt.

<img src="./media/image130.png"
style="width:6.26806in;height:2.25625in" />

<img src="./media/image131.png"
style="width:6.26806in;height:2.39097in" />

### Conclusion

By completing this exercise, participants will learn:

- Successfully tested the trigger by manually submitting the Employee
  Onboarding Form.

- Ensured the connection was established and tested properly.

- Verified the flow actions were triggered correctly upon form
  submission, with all connections and permissions successfully set up.
