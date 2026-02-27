# BookBuddy

This is my capstone project at GMU. This BookBuddy application was developed to assist an aspiring author in promoting the content of her new book. The application offers three key functionalities:  
(1) AI-powered image and text generation,  
(2) web scraping to analyze search trends based on user-provided prompts.  
(3) A business finance tracker that enables users to input and delete financial records while keeping track of monthly and total expenses.  

The frontend of this application was developed using **Tkinter**, and the backend was developed using **Python**.

Please note, running this application requires subscriptions to Google Search API (SerpApi) and Open API with having money in the OpenAI account. More information in the document below.

<img width="786" height="230" alt="image" src="https://github.com/user-attachments/assets/f8384a73-3931-45e2-b533-28cd02c81cd2" />
<img width="365" height="413" alt="image" src="https://github.com/user-attachments/assets/3277971d-5ecd-4aaf-9882-0ee795849612" />
<img width="352" height="386" alt="image" src="https://github.com/user-attachments/assets/e10298b8-b5ce-4641-8982-0ae84a9e11c5" />
<img width="545" height="232" alt="image" src="https://github.com/user-attachments/assets/752cd3fd-a097-4b70-9444-c758c244e3ad" />

----------

Book Buddy

Section #	   Topic	                 

1	           Introduction	               	    

2              System Setup	                   

3              System Overview	           

4	           Security                         

5              Interface Design                 

6              Troubleshooting and Help	    

Section 1: Introduction

Welcome to the Book Buddy Training Documentation. This manual serves as your comprehensive guide, covering everything from the initial setup of your Book Buddy to troubleshooting the application. Whenever relevant, we will provide links and supplemental resources to enhance your understanding and implementation. For any queries regarding the software, please consult this document as your primary reference resource. Let's embark on this journey together to maximize your Book Buddy experience.

Section 2: System Setup

Local Resources and downloads needed prior to using Book Buddy.

1.	On the main project page for ‘Capstone,’ click on BookBuddy.py. To download the stable version of BookBuddy.py, click on development to open a drop down menu, then select master. Then, click the download icon (an arrow pointing down into a sideways bracket). (This contains all of the system code).
2.	Click on Capstone to return to the main project page.
3.	Click on requirements.txt. Click on the download icon described in step 2 (this contains all of the modules you will need to install, instructions in a later section).

Download Python  
*Skip this step if a Python 3 variation is already installed on your computer. Python 2 variations ARE NOT compatible with the program.*

1.	Navigate to https://www.python.org/downloads/  
2.	Click the yellow button “Download Python <latest version>” (at time of writing, that is 3.12.2).  
3.	Open Installer File that was saved to downloads.  
4.	Go through setup, selecting the option “Install Now” unless customized install is necessary.  
5.	With the exception of selecting the “Add python.exe to path” option, remain on default options.  
6.	When prompted to “Disable path length limit,” click on close to finish the installation.

Download PyCharm Community  
Skip this step if Pycharm is already installed on your computer. Pycharm Professional also works (additional charge), however it is not needed for Book Buddy to operate. Refer to Section 5: Troubleshooting and Help for a video tutorial on setting up Pycharm.

Pycharm is an essential IDE for Book Buddy to work. Book Buddy has been tested using Visual Studio code, which is not functional. Please always remember to run Book Buddy in Pycharm.

1.	Navigate to https://www.jetbrains.com/pycharm/download/other.html in a web browser.  
2.	Download the PyCharm Community Edition variation “Windows (exe)” by clicking on the option matching it (at time of writing, “2023.3.5 - Windows (exe)”).  
3.	Open Installer File that was saved to downloads.  
4.	Go through setup, keeping all default options.  
5.	Exit the Installer.

Setup SerpAPI  

1.	Navigate to https://serpapi.com/  
2.	Click Sign in or Register if you are a new user.  
3.	Once you see your account dashboard, click “API Key” in the left vertical nav bar. The free plan allows for 100 searches a month unless you upgrade your account which allows more.  
4.	Copy the API Key.  

Setup OpenAI API Key  

1.	Navigate to https://openai.com/  
2.	Either create an account, following the instructions on the website, or login with an existing account.  
3.	When logged in, there will be two choices, click the “API” option.  
4.	Click the lock icon on the left vertical nav menu.  
5.	Click on the button that says “create new secret key.”  
6.	Follow the prompt.  
7.	Before clicking create, be sure to write the password down somewhere safe and secure for reference. After the key is created, this is the only time it will be available to see and write down.  
8.	Create the key.  

Add money to OpenAI Account  

1.	Navigate https://openai.com/blog/openai-api  
2.	Login to OpenAI account.  
3.	Click on “Settings” in the left vertical nav bar.  
4.	Click on “billing.”  
5.	Click “Add credit balance.”  
6.	Add the desired amount to your account.  
   - Note: Adding 10 dollars will give up to 250 image generations or 5000 sets of text generation (up to 750 words each set). These values are the maximum if that is the only type being performed, mixing and matching the generation type will result in lower numbers for both.

Setup SQL Server  

1.	Steps 2–6 can be skipped if the system already has the following installed:  
   - Visual Studio 2019 x64 redistributable  
   - Microsoft Visual C++ 14.0 or greater  
2.	Navigate to https://visualstudio.microsoft.com/downloads/  
3.	Download the ‘Community’ version of Visual Studio 2022 by clicking ‘Free download’.  
4.	Run the Visual Studio Installer.  
5.	In the Desktop & Mobile section, click the checkmark for ‘Desktop development with C++,’ then click install in the bottom right corner.  
6.	Once the install has finished, close the Visual Studio Installer.  
7.	Navigate to https://dev.mysql.com/downloads/mysql/  
8.	Download the ‘Windows (x86, 64-bit), MSI Installer’ by clicking the associated download button.  
9.	Follow the installer prompt, installing the ‘Typical setup’ option, unless otherwise necessary.  
10.	Be sure to write the username and password down somewhere safe and secure for your reference. You will need this in a later section.  

Setup Project  

1.	Open Pycharm.  
2.	Create a new project.  
3.	Name the project (ex: BookBuddyProject).  
4.	Click and drag the BookBuddy.py file and Requirements.txt file from your downloads folder to the left hand project window in PyCharm.  
5.	Open a new terminal.  
6.	Run this command: pip install -r requirements.txt  
7.	Run this command, replacing the red with your keys:  

```
encryptoenv -a "OpenAIKey=InsertHere" "PASSWORD=InsertHere" "SerpAPI=InsertHere" -E
```

- OpenAIKey is the API key from OpenAI.  
- PASSWORD is the SQL database password.  
- SerpAPI is the API key from SerpAPI.  

8.	In Pycharm, modify the variables “HostNameVar” “userVar” and “Passwordvar” to match what you wrote down.  
9.	Now you should be ready to run Book Buddy. If you have encountered any errors please refer to Section 5: Troubleshooting and Help.  
10.	Run the code.  
11.	If errors occur, ensure the previous steps were followed correctly. Otherwise, the Book Buddy Landing page should appear.  

Section 3: Security

General Password Security  

Requirements:  
- 14+ characters long  
- At least one uppercase letter  
- At least one lowercase letter  
- At least one number  
- At least one symbol  
- Cannot have 5+ occurrences of the same character  
- Changed annually  

(Windows account, MySQL password, system access, and lock procedures remain unchanged as originally written.)

Section 4: Interface Design

Wireframes of the Book Buddy Interface design. This section serves as a reference of the Book Buddy Interface architecture.  

Wireframes can be found here:  
https://www.figma.com/file/xndBfBaQ2EkMOfibfpiw2S/Book-Buddy-Interface-Design  

Section 5: Troubleshooting and Help

Errors that you may encounter, plus some external resources.  

Most common fixes include:  
- Delete your old env file  
- Ensure SQL Server is properly set up  
- Use the most up-to-date version of Book Buddy  
- Redownload Python  
- Ensure the encrypt command was configured correctly  

Book Buddy only works on Windows operating system and must be run in PyCharm.  

Additional troubleshooting steps and error explanations remain as originally written above.
